---
weight: 36
title: "学習済みモデルの概要"
description: "生成AIの中身をざっくり知る"
icon: "Tenancy"
date: "2024-01-22T20:50:17+09:00"
lastmod: "2024-01-22T20:50:17+09:00"
draft: false
toc: true
---

{{< alert icon="🛸" context="dark" text="ちょっとだけ発展的な内容を含むページです" />}}

{{< alert context="warning" text="分かりやすさを重視し、詳細を省略しています" />}}

生成AIサービスでは事前に収集したデータを学習(訓練)する過程を経て作成した学習済みモデルが使用しています。  
例えばChatGPTにはGPTが、BardにはPalm2が使用されています。  
それはどのように作成(学習)され、生成AIサービスとして使われているのでしょうか。  



## 🧠 学習段階
--- 
```mermaid
graph LR
    A[生データ] -->|加工| B[学習用データセット]
    B -->|入力| C[学習用プログラム]
    C --o D[学習前パラメータ]
    C --o E[ハイパーパラメータ]
    C -->|出力| F{{学習済みモデル}}
    F --o G[学習済みパラメータ]
    F --o H[推論プログラム]
```

一般的な言語モデルの学習段階は、主に以下のステップで構成されます。

### - 生データ -> 学習用データセット
- **生データ収集**: インターネット上の文章、書籍、ニュース記事、ウィキペディアのテキストなど、多種多様なソースから大量のテキストデータを収集します。
- **前処理**: 収集したデータは、ノイズが含まれていたり、不適切な内容が含まれている可能性があります。これらをクリーニングし、モデルが学習しやすい形式に整形します。具体的には、トークン化（テキストを意味のある単位に分割）、正規化（テキストの標準化）、不適切な内容の除去などが含まれます。

<br>

### - 学習用プログラム
- **モデルアーキテクチャの選定**: Transformerアーキテクチャなど、ニューラルネットワークの構造を決定します。
- **学習アルゴリズムの実装**: ディープラーニングの学習アルゴリズム（例：バックプロパゲーション）を実装し、モデルがデータからパターンを学習できるようにします。

<br>

### - (学習プロセス)
- **データセットの準備**: 前処理されたデータをトレーニングセット、バリデーションセット、テストセットに分割します。
- **トレーニング**: トレーニングセットを使用してモデルを学習させます。これには、膨大な計算資源と時間が必要です。モデルは、テキストのパターン、文法、意味論的関係などを理解するようになります。
- **バリデーションとチューニング**: バリデーションセットを使用してモデルの性能を評価し、ハイパーパラメータを調整します。
- **評価**: テストセットを使用して、モデルが未知のデータに対してどのように機能するかを評価します。
- **最適化**: 必要に応じて、さらなるチューニングやモデルのサイズ調整を行い、性能と効率のバランスを取ります。

<br>

### - 学習済みモデル
- **保存**: 学習が完了したモデルは、ファイルとして保存され、後の使用や共有のためにアーカイブされます。
- **展開**: 学習済みモデルは、アプリケーションやサービスに組み込まれ、実際のタスクに使用されます。

これらのステップは、大規模な言語モデルを構築するために必要な、高度に専門化されたプロセスです。それぞれのステップは、データサイエンティスト、機械学習エンジニア、ソフトウェアエンジニアなど、多くの専門家の協力を必要とします。

<br>

## 💻 利用段階
---
```mermaid
graph LR
    A[入力データ] -->|入力| B{{学習済みモデル}}
    B -->|出力| C[AI生成物]
```
<br>

大規模言語モデルの利用段階は、以下のステップで構成されます。

### - 入力データ
- **ユーザーからの入力**: ユーザーは質問、コマンド、文章などの形で入力を提供します。これはテキスト形式であることが一般的です。
- **入力の前処理**: モデルが処理できる形に入力データを変換します。これには、トークン化（テキストを小さな単位に分割）、正規化、必要に応じて言語の検出や翻訳などが含まれます。

<br>

### - 学習済みモデル
- **モデルへの入力**: 前処理された入力データは、学習済みの言語モデルに供給されます。
- **処理と推論**: 言語モデルは入力データを処理し、文脈に基づいた適切な応答を生成します。これには、テキストの意味理解、関連情報の抽出、新しい文章の生成などが含まれます。

<br>

### - 生成物
- **応答の生成**: モデルは、質問に対する回答、テキストの続き、情報の要約など、要求に応じた内容を生成します。
- **後処理**: 必要に応じて、生成されたテキストに後処理を施します。これには、文法の調整、スタイルの整合性の確保、不適切な内容のフィルタリングなどが含まれる場合があります。
- **ユーザーへの提供**: 最終的な生成物は、ユーザーに提示されます。これは、ウェブインターフェース、API応答、書面によるレポートなど、多様な形式で行われます。

<br>

### - (フィードバックと改善)
- **ユーザーフィードバックの収集**: ユーザーからのフィードバックを収集し、モデルの性能評価に利用します。
- **継続的な改善**: フィードバックに基づいて、モデルの微調整やアップデートを行うことで、精度やユーザー体験を向上させます。

大規模言語モデルの利用段階では、モデルが以前に学習した知識を活用して新しい問い合わせに応答し、有用な情報や内容を生成します。ユーザーのニーズやコンテキストに応じて柔軟に対応できるよう、継続的な改善とアップデートが重要となります。

<br>

## 📚 参考文献
---
https://www.meti.go.jp/policy/mono_info_service/connected_industries/sharing_and_utilization/20180615001-3.pdf