---
weight: 37
title: "生成AIとツールの連携"
description: "外部ツールと生成AIの関係を理解する"
icon: "Extension"
date: "2024-01-21T19:24:51+09:00"
lastmod: "2026-02-12T00:00:00+09:00"
draft: false
toc: true
---

{{< alert icon="🛸" context="dark" text="発展的な内容を含むページです" />}}

{{< alert context="warning" text="分かりやすさを重視し、詳細を省略しています" />}}

ChatGPTで使用されているAIモデルが[WebAPIで公開](https://openai.com/blog/introducing-chatgpt-and-whisper-apis)されており、従量課金制で誰でも利用できます。ChatGPTだけではなくClaudeやGeminiもWebAPIを公開しています。WebAPIを叩けると、技術者が泣いて喜びます。なぜなら生成AIの内部モデルを別のサービスやシステムに組み込むことができるからです。<strong>その最たる例がMicrosoftのCopilotです。</strong>従来の検索エンジンにLLMを使用することで、Webサイトの情報を利用者へ素早く・分かりやすく提供しています。


そのほか、こうした「AIモデルを組み込んだサービス」は[星の数](https://aismiley.co.jp/ai_news/generativeai-chaosmap/)ほどあります。そのすべてを紹介することはできませんので、メジャーな生成AIサービスの類型を紹介します。

## 🗂️ 生成AIサービスの類型
---
<br>

### - 基本型
#### LLM[外部ツール無し]
例：ChatGPT、Claude

Web検索に対応していない生成AIサービスです。このほか、例えば会議の議事録を要約するサービスが該当します。


```mermaid
    sequenceDiagram
    box rgb(221,255,221) 利用者 🙂
    actor 大学職員
    end
    box インターフェース 🖥️
    participant サービス画面
    end
    box バックエンド ⚙️
    participant LLM
    end
    大学職員->>サービス画面: 1.プロンプトを投げる
    サービス画面->>LLM: 2.クエリを投げる
    LLM->>サービス画面: 3.レスポンスを返す
    サービス画面->>大学職員: 4.回答を出力する
```

<br>

### - 検索エンジン型
#### LLM+Web検索
例：Copilot、Gemini、Perplexity

検索エンジンが搭載された生成AIサービスです。無料で高性能なAIモデルを活用できるケースも多いため、ChatGPTではなくこちらを積極的に活用している方もいます。

```mermaid
    sequenceDiagram
    box rgb(221,255,221) 利用者 🙂
    actor 大学職員
    end
    box インターフェース 🖥️
    participant サービス画面
    end
    box バックエンド ⚙️
    participant バックエンドプログラム
    participant Web検索
    participant LLM
    end
    大学職員->>サービス画面: プロンプトを投げる
    サービス画面->>バックエンドプログラム: チャット内容を送信
    バックエンドプログラム->>Web検索: チャット内容をもとにクエリを作成・検索
    Web検索->>バックエンドプログラム: 検索結果の回答
    バックエンドプログラム->>LLM: 質問＋検索結果
    LLM->>バックエンドプログラム: LLMによる回答
    バックエンドプログラム->>サービス画面: 回答の送信
    サービス画面->>大学職員: 結果を受信
```

<br>


### - ナレッジ参照型
#### LLM+ドキュメント
例：窓口応答システム、社内文書システム等

無料かつWeb公開されているサービスではほぼ見られませんが、LLMの訓練データを超えたデータを埋め込むタイプの生成AIサービスがあります。特に一般向け・社内向けに整備されたものが多い印象です。


```mermaid
    sequenceDiagram
    box rgb(221,255,221) 利用者 🙂
    actor 大学職員
    end
    box インターフェース 🖥️
    participant サービス画面
    end
    box バックエンド ⚙️
    participant バックエンドプログラム
    participant ドキュメントの参照
    participant LLM
    end
    大学職員->>サービス画面: プロンプトを投げる
    サービス画面->>バックエンドプログラム: チャット内容を送信
    バックエンドプログラム->>ドキュメントの参照: チャット内容をもとにクエリを作成・検索
    ドキュメントの参照->>バックエンドプログラム: 検索結果の回答
    バックエンドプログラム->>LLM: 質問＋検索結果
    LLM->>バックエンドプログラム: LLMによる回答
    バックエンドプログラム->>サービス画面: 回答の送信
    サービス画面->>大学職員: 結果を受信
```

<br>


### - 自律エージェント型(1)
#### LLM+自律的な推論と行動
例：AutoGPT（初期の代表例）、現在の各種AIエージェント

AIエージェントとは、**AIが自ら考え、ツールを使い、タスクを遂行する仕組み**です。利用者が目標を与えると、AIが自律的に計画を立て、必要な情報を集め、結論を導きます。利用者としてエージェントに仕事を任せる考え方は[AIエージェントとタスク設計]({{% relref "/docs/intermediate/agent-task-design" %}})で紹介しています。

2023年に登場したAutoGPTは、LLMに「思考→行動→観察」のループ（ReActパターン）を繰り返させる初期の代表例でした。現在では、ChatGPT・Claude・Geminiなどの主要サービスに同様の仕組みが標準的に組み込まれています。

```mermaid
    sequenceDiagram
    box rgb(221,255,221) 利用者 🙂
    actor 大学職員
    end
    box インターフェース 🖥️
    participant サービス画面
    end
    box バックエンド ⚙️
    participant バックエンドプログラム
    participant Web検索
    participant LLM
    end
    大学職員->>サービス画面: プロンプトを投げる
    サービス画面->>LLM: チャット内容を送信
    loop 結論が出るまで繰り返す
    LLM->>バックエンドプログラム: 思考・行動を決定
    バックエンドプログラム->>Web検索: 検索を実行
    Web検索->>バックエンドプログラム: 検索結果（観察）
    バックエンドプログラム->>LLM: 結果をもとに次の行動を判断
    end
    LLM->>バックエンドプログラム: 最終回答
    バックエンドプログラム->>サービス画面: 回答の送信
    サービス画面->>大学職員: 回答を出力する
```

<br>


### - 自律エージェント型(2)
#### LLM+コード実行環境

ChatGPTやClaudeなどの主要な生成AIサービスには、**自然言語のプロンプトからプログラムを作成・実行する機能**が搭載されています。利用者がコードを書けなくても、データ分析やグラフ作成などをAIに任せることができます。

例えばChatGPTでは「データ分析」機能（旧称：Code Interpreter）として、Claudeでは「Artifacts」として、こうしたコード実行機能が提供されています。


```mermaid
    sequenceDiagram
    box rgb(221,255,221) 利用者 🙂
    actor 大学職員
    end
    box インターフェース 🖥️
    participant サービス画面
    end
    box バックエンド ⚙️
    participant LLM
    participant コード実行環境
    end
    大学職員->>サービス画面: プロンプトを投げる
    サービス画面->>LLM: チャット内容を送信
    LLM->>LLM: プログラムの作成
    LLM->>コード実行環境: プログラムの送信
    コード実行環境->>コード実行環境: プログラムの実行
    alt is ERROR
        loop 繰り返し
        コード実行環境->>LLM: エラーの送信
        LLM->>LLM: プログラムのデバッグ
        LLM->>コード実行環境: プログラムの送信
        end
    else is WELL
        コード実行環境->>LLM: 実行結果の返却
    end
    LLM->>サービス画面: 回答の送信
    サービス画面->>大学職員: 回答を出力する
```

<br>


### - AIエージェントの発展
#### LLM+複数のツール・データソース

現在のAIエージェントは、Web検索やコード実行だけでなく、**様々な外部ツールやデータソースと連携**できるようになっています。

例えばChatGPTの「GPTs」では、利用者が目的に合わせたカスタムAIを作成でき、Claudeの「Projects」では、ドキュメントを参照しながら対話できます。こうしたユーザー向け機能の充実により、専門知識がなくてもAIエージェントの恩恵を受けやすくなりました。

また技術的な基盤として、**MCP（Model Context Protocol）** という共通規格が登場しています。MCPは、様々なツールやデータソースをAIに接続するための共通規格です。これにより、AIサービス間で統一的にツール連携が行えるようになりつつあります。

```mermaid
sequenceDiagram
    box rgb(221,255,221) 利用者 🙂
    actor 大学職員
    end
    box インターフェース 🖥️
    participant AIエージェント画面
    end
    box バックエンド ⚙️
    participant LLM
    participant ツール群
    end
    大学職員->>AIエージェント画面: 目標・指示を投げる
    AIエージェント画面->>LLM: 指示を送信
    loop タスク完了まで繰り返す
    LLM->>LLM: 計画の立案・見直し
    LLM->>ツール群: 必要なツールを選択・実行
    ツール群->>LLM: 実行結果を返却
    end
    LLM->>AIエージェント画面: 最終的な成果物を送信
    AIエージェント画面->>大学職員: 成果物を出力する
```

2025年以降、Manus、Claude Code、Devinなどのエージェント型ツールが登場し、AIがより複雑なタスクを自律的にこなせるようになりつつあります。こうしたツールは今後も増えていくと考えられますが、基本的な仕組み（LLMがツールを選択・実行するループ）は上記の構造と同じです。なお、エージェントの推論能力を支える「推論モデル」については[推論モデルを知る]({{% relref "/docs/essence/reasoning-models" %}})で解説しています。

{{% alert icon="" context="info" %}}
AIエージェントが発展しても、<strong>最終的な判断と責任は利用者にある</strong>という原則は変わりません。AIが自律的に動くからこそ、結果の確認と適切な指示がより重要になります。
{{% /alert %}}


## 📚 参考文献
https://speakerdeck.com/hirosatogamo/chatgpt-azure-openai-da-quan?slide=29