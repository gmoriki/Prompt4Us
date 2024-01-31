---
weight: 35
title: "生成AIとツールの連携"
description: "外部ツールと生成AIの関係を理解する"
icon: "Extension"
date: "2024-01-21T19:24:51+09:00"
lastmod: "2024-01-21T19:24:51+09:00"
draft: false
toc: true
---

{{< alert icon="🛸" context="dark" text="発展的な内容を含むページです" />}}

{{< alert context="warning" text="分かりやすさを重視し、詳細を省略しています" />}}

ChatGPTの中で使用されてるAIモデル(GPT-3.5やGPT-4)が[WebAPIで公開](https://openai.com/blog/introducing-chatgpt-and-whisper-apis)されており、従量課金制で誰でも利用できます。ChatGPTだけではなくClaudeやGeminiもWebAPIを公開しています。WebAPIを叩けると、技術者が泣いて喜びます。なぜならChatGPT内部のAIモデルを別のサービスやシステムに組み込むことができるからです。<strong>その最たる例がMicrosoftのCopilot(旧Bing AI)です。</strong>従来の検索エンジンにLLMを使用することで、Webサイトの情報を利用者へ素早く・分かりやすく提供しています。


そのほか、こうした「AIモデルを組み込んだサービス」は[星の数](https://aismiley.co.jp/ai_news/generativeai-chaosmap/)ほどあります。そのすべてを紹介することはできませんので、メジャーな生成AIサービスの類型を紹介します。

## 🗂️ 生成AIサービスの類型
---
<br>

### - 基本型
#### LLM[外部ツール無し]
例：ChatGPT(無料版)、Claude

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
例：Copilot(旧Bing AI)、Bard、Perprexity

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
#### LLM+Web検索+ReAct
例：AutoGPT

LLMを活用して自律エージェントを実装した例も見られます。これは一例で、現在も開発が活発だと見受けられます。

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
    LLM->>バックエンドプログラム: ReAct形式に変換(思考、行動、観察)
    バックエンドプログラム->>Web検索: 検索結果の回答
    Web検索->>バックエンドプログラム: 検索結果(観察)
    バックエンドプログラム->>LLM: 検索結果をReAct形式に変換
    end
    LLM->>バックエンドプログラム: 最終回答
    バックエンドプログラム->>サービス画面: 回答の送信
    サービス画面->>大学職員: 回答を出力する
```

<br>


### - 自律エージェント型(2)
#### LLM+Python実行環境
例：Code Interpreter、Open Interpreter

ChatGPT Plus加入者であれば身に覚えのある「Code Interpreter」や、その欠点を補うオープンソースソフトウェア「Open Interpreter」が該当します。自然言語のプロンプトを投げるだけでプログラムの作成・実行・デバッグを行う優れものです。


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
    participant Python実行環境
    end
    大学職員->>サービス画面: プロンプトを投げる
    サービス画面->>LLM: チャット内容を送信
    LLM->>LLM: プログラムの作成
    LLM->>Python実行環境: プログラムの送信
    Python実行環境->>Python実行環境: プログラムの実行
    alt is ERROR
        loop 繰り返し
        Python実行環境->>LLM: エラーの送信
        LLM->>LLM: プログラムのデバッグ
        LLM->>Python実行環境: プログラムの送信
        end
    else is WELL
        Python実行環境->>LLM: 実行結果の返却
    end
    LLM->>サービス画面: 回答の送信
    サービス画面->>大学職員: 回答を出力する
```

<!-- 
### 今後の生成AIサービス
```mermaid
sequenceDiagram
    box 利用者
    actor 大学職員
    end
    box AIエージェント
    participant エージェント画面
    participant サービス画面
    participant LLM
    end
    大学職員->>エージェント画面: プロンプトを投げる
    エージェント画面->>サービス画面: 必要なサービスを選択し、クエリを投げる
    サービス画面->>LLM: クエリを投げる
    LLM->>サービス画面: レスポンスを返す
    サービス画面->>エージェント画面: 回答を返す
    エージェント画面->>大学職員: 回答を出力する

``` -->


## 📚 参考文献
https://speakerdeck.com/hirosatogamo/chatgpt-azure-openai-da-quan?slide=29