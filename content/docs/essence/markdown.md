---
weight: 34
title: "基本的なマークダウン記法"
description: "生成AIとの円滑なコミュニケーションのために"
icon: "Subtitles"
date: "2024-01-20T05:57:52+09:00"
lastmod: "2024-01-20T05:57:52+09:00"
draft: false
toc: true
---
ChatGPTをはじめとして、多くの生成AIでは<strong>マークダウン記法</strong>が採用されています。
{{% alert icon="📖" context="light" %}}
マークダウンは、プレーンテキスト文書にフォーマット要素を追加するために使用できる軽量マークアップ言語です。2004年にジョン・グルーバーによって作成されたマークダウンは、現在世界で最も人気のあるマークアップ言語の一つです。例えば、見出しを示すために、それの前にナンバーサインを追加します（例：# 見出し1）。または、フレーズを太字にするために、それの前後に2つのアスタリスクを追加します（例：このテキストは太字です）。  
参考：[Markdown Guide Getting Started(運営者による日本語訳)](https://www.markdownguide.org/getting-started/)
{{% /alert %}}

{{< table "table-responsive" >}}
| 日時 | このページで使用した生成AI | 
|----------|--------------|
| 2024/1/20 | ChatGPT(GPT-4) |
{{< /table >}}

<br>


## 🎯 マークダウン基本ガイド
---

### - 見出し

マークダウンでは、`#` を使って見出しを作成します。`#` の数で見出しのレベルが決まります。例えば、

```markdown
# 見出し1
## 見出し2
### 見出し3
```

これらはそれぞれ見出し1、見出し2、見出し3に相当します。

<br>

### - 太字

太字にするには、単語の両側を `**` または `__` で囲みます。例えば、

```markdown
**このテキストは太字です**
__これも太字です__
```

<br>


### - リスト

項目の先頭に `-` や `*` を置くことで、番号なしリストを作成できます。例えば、

```markdown
- リスト項目1
- リスト項目2
```
<br>


### - 番号付きリスト

番号付きリストは項目の先頭に数字とピリオドを置くことで作成できます。例えば、

```markdown
1. 最初の項目
2. 次の項目
```

<br>


### - テーブル

| と - を使ってテーブルを作成できます。例えば、

```markdown
| ヘッダ1 | ヘッダ2 | ヘッダ3 |
| ------- | ------- | ------- |
| 行1    | データ  | データ  |
| 行2    | データ  | データ  |
```

<br>


### - コードブロック

コードやコマンドを示す際には、バッククォート ``` を3つ使用してコードブロックを作成します。例えば、

````markdown
```
この中にコードを書きます
```
```````

<br>


### - 引用ブロック

> 引用を示す際には、行の先頭に `>` を置きます。例えば、

```markdown
> これは引用ブロックです。
```

<br>


### - 水平線

水平線は `---` または `___` で作成できます。これはセクションを分割するのに便利です。例えば、

```markdown
---
```

<br>

--- 

これで基本的なマークダウンの文法についての説明は終わりです。これらの要素を組み合わせて、効果的に文書を整理し、見やすくすることができます。  
ChatGPTの生成物に使われるだけではなく、プロンプトの構造的な書き方にも大きな影響を与えているので、最低限の記法をおさえておきましょう。  

なおこのページはほとんどChatGPT(GPT-4)の生成物です。  
https://chat.openai.com/share/fb6f2212-5821-4ba8-b616-55754f58cb35  

