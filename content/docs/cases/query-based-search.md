---
weight: 67
title: "Copilotで英語圏の情報を収集する"
description: "上手なWeb検索"
icon: "article"
date: "2024-01-30T15:39:50+09:00"
lastmod: "2024-01-30T15:39:50+09:00"
draft: false
toc: true
---

Microsoftの蒲生さんがTwitterで共有されたテクニックです。

{{< table "table-responsive" >}}
| 日時 | このページで使用した生成AI | 
|----------|--------------|
| 2024/1/30 | Copilot(GPT-4) |
{{< /table >}}

```
プロンプトエンジニアリングガイドとは何か。
英語で検索クエリを作成し、回答は日本語で出力して
```
<br>

![英語でクエリを作成](images/query-based-search.png)

<br>

{{% alert icon="🤖" context="success" %}}
プロンプトエンジニアリングガイドは、大規模な言語モデル（GPTモデルとも呼ばれる）からより良い結果を得るための戦略と戦術を共有するガイドです¹。これは、マシン学習モデルが正確な出力を生成するように導く高品質なプロンプトを設計することを含みます³⁵。

以下に、より良い結果を得るためのいくつかの戦略を示します¹：
- **明確な指示を書く**：モデルはあなたの心を読むことはできません。出力が長すぎる場合は、簡潔な返答を求めます。出力が単純すぎる場合は、専門レベルの文章を求めます。フォーマットが気に入らない場合は、見たいフォーマットを示します。モデルがあなたが何を望んでいるかを推測する必要が少なければ少ないほど、あなたが望むものを得る可能性が高くなります。
- **複雑なタスクをより単純なサブタスクに分割する**：ソフトウェアエンジニアリングで複雑なシステムを一連のモジュラーコンポーネントに分解するのが良い実践であるのと同様に、言語モデルに提出されるタスクについても同じことが言えます。複雑なタスクは、より単純なタスクよりもエラー率が高い傾向があります。さらに、複雑なタスクは、初期のタスクの出力を使用して後のタスクの入力を構築するような、より単純なタスクのワークフローとして再定義できることがよくあります。
- **モデルに「考える」時間を与える**：17と28を掛けるように求められた場合、あなたはすぐに答えを知らないかもしれませんが、時間をかけて答えを出すことができます。同様に、モデルは、すぐに答えを出そうとすると、より多くの推論エラーを犯す傾向があります。答えの前に「思考の連鎖」を求めることで、モデルはより確実に正しい答えにたどり着くための推論を行うことができます。

これらの方法は、組み合わせて使用することで効果を発揮することがあります¹。また、これらの方法は、特定のタスクに最適な方法を見つけるための実験を奨励しています¹。⁴でも日本語での試用例が紹介されています。²では、DAIR.AIによるプロンプトエンジニアリングガイドのプロジェクトが紹介されており、研究者や実践者にプロンプトエンジニアリングについて教育することを目指しています。

ソース: Bing との会話 2024/1/30  
(1) Prompt engineering - OpenAI API. https://platform.openai.com/docs/guides/prompt-engineering/prompt-engineering.  
(2) What Is Prompt Engineering? Definition and best practices .... https://www.educative.io/blog/what-is-prompt-engineering.  
(3) What is prompt engineering? | IBM. https://www.ibm.com/topics/prompt-engineering.  
(4) OpenAIのPrompt Engineering Guideでより良い結果を得る .... https://zenn.dev/zuma_lab/articles/openai-prompt-engineering-guide.  
(5) About | Prompt Engineering Guide. https://www.promptingguide.ai/about.  
{{% /alert %}}


```
プロンプトエンジニアリングガイドを提供しているWebページを10個挙げて。
英語で検索クエリを作成し、回答は日本語で出力して
```

今回のクエリは**Websites providing the Prompt Engineering Guide**です。

{{% alert icon="🤖" context="success" %}}
以下に、プロンプトエンジニアリングガイドを提供しているウェブページをいくつか紹介します：
1. [OpenAI API](^1^)：OpenAIの公式APIドキュメント内にあるプロンプトエンジニアリングガイドです。大規模な言語モデルからより良い結果を得るための戦略と戦術を共有しています¹。
2. [Gihyo.jp](^2^)：DAIR.AIが公開しているプロンプトエンジニアリングガイドの日本語訳が公開されています²。
3. [Zenn.dev](^3^)：OpenAIのプロンプトエンジニアリングガイドを日本語で試したり、自分なりに応用して実践してみる記事が掲載されています³。

ただし、現時点では検索結果から得られたウェブページは3つだけです。他のウェブページについては、具体的なウェブサイト名やURLが必要な場合は、それらの情報を提供していただければと思います。それにより、より具体的な検索を行うことが可能となります。ご理解いただけますと幸いです。¹²³

ソース: Bing との会話 2024/1/30  
(1) Prompt engineering - OpenAI API. https://platform.openai.com/docs/guides/prompt-engineering/prompt-engineering.  
(2) Prompt engineering - OpenAI API. https://platform.openai.com/docs/guides/prompt-engineering/prompt-engineering.  
(3) 「Prompt Engineering Guide」の日本語訳が公式サイトにマージ .... https://gihyo.jp/article/2023/04/prompt-engineering-guide.  
(4) 「Prompt Engineering Guide」の日本語訳が公式サイトにマージ .... https://gihyo.jp/article/2023/04/prompt-engineering-guide.  
(5) OpenAIのPrompt Engineering Guideでより良い結果を得る .... https://zenn.dev/zuma_lab/articles/openai-prompt-engineering-guide.  
(6) OpenAIのPrompt Engineering Guideでより良い結果を得る .... https://zenn.dev/zuma_lab/articles/openai-prompt-engineering-guide.  
{{% /alert %}}
