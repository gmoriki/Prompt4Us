---
weight: 999
title: "外部ツールとの連携"
description: "外部ツールと生成AIの関係を理解する"
icon: "article"
date: "2024-01-21T19:24:51+09:00"
lastmod: "2024-01-21T19:24:51+09:00"
draft: true
toc: true
---

このページで作図は多くの技術的要素を省略しています


- 生成AIサービスに含まれるツール
- 検索エンジンと生成AI
- プログラム実行環境と生成AI
- 画像生成AIとテキスト生成AI
- RAGと生成AI




<br>

### 通常の対話型生成AIサービス
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
    大学職員->>サービス画面: プロンプトを投げる
    サービス画面->>LLM: クエリを投げる
    LLM->>サービス画面: レスポンスを返す
    サービス画面->>大学職員: 回答を出力する
```

### 検索型・対話型生成AIサービス
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

```


参考URL
https://speakerdeck.com/hirosatogamo/chatgpt-azure-openai-da-quan?slide=29