---
weight: 999
title: "Test"
description: ""
icon: "article"
date: "2024-01-19T12:34:35+09:00"
lastmod: "2024-01-19T12:34:35+09:00"
draft: true
toc: true
---


{{% alert icon="" context="info" %}}
<strong>P4Usは、生成AI利用の文化を理解し、プロンプトを学ぶための(ゆる)プロンプトガイドです。</strong>  
「固すぎず柔らかすぎない」「難しすぎず易しすぎない」程度に日常的なプロンプトやプロンプトに関するknown issue、ノウハウ、また作成者が講演・ワークショップで使用(収集)したプロンプトを掲載しています。

例えば以下のページでは、2023年開催のMJIRのハンズオン講演で使用したプロンプトを掲載しています。


<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../archive/irprompt/">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Bar_Chart</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">MJIR2023講演</p>
        <p class="para card-text mb-0">「大学IRにおける生成AI利用の試み」</p>
      </div>
    </div>
  </a>
</div>

</div>
{{% /alert %}}
  
  
## 🔰 P4Usの使い方
---
### - プロンプトを使ってみる

掲載している全てのプロンプトは右上のアイコンからコピー&ペーストが可能です。

```
右上の「コピーアイコン」をクリックしてください。
ここに記載しているテキストがコピーされるので、
あとは張り付けるだけって寸法です。
```

<strong>大量！</strong>ではありませんが、それなりに、様々なプロンプトを用意しています。
- 各情報源から収集したプロンプト
- 作成者が日々使っているプロンプト
- gmorikiが生成AIに関する講演の中で使用したプロンプト
- gmorikiがワークショップ参加者より収集したプロンプト

ぜひプロンプトを実際に使ってみてください。



### プロンプトが全てではないと悟る

俗にいう「プロンプトエンジニアリング」を体系的に習得することが目的ではありません。

> AI（人工知能）から望ましい出力を得るために、指示や命令を設計、最適化するスキルのことです。ChatGPTなどの生成AIを使いこなすために注目されるようになりました。生成AIは、命令（プロンプト）の出し方によって、出力されるコンテンツの質が大きく異なるため、より適切なものを入力するスキルが求められています。  
参考：[野村総合研究所 プロンプトエンジニアリング](https://www.nri.com/jp/knowledge/glossary/lst/ha/prompt_engineering)


P4Usは大層な教材を提供するわけではありませんが、「ChatGPTに指示を出せと言われてもどうすればいいのか全く分からんよ」という方がチラ見すると役立つかもしれない資料集です。「こんなことできんの」「もっとこうしたい」「思ってたよりザコやな」などと考え、実際に指示を出す過程をそれとなくサポートします。

生成AI利用の体系を公表した身としては、ただ触るだけが「生成AIを利用するための」リテラシーではありません。しかしただ触ることすらままならない大学さんが多い現状を受けて、リテラシーの入口の場が必要なのかも、と考えました。




プロンプトエンジニアリングは一般ユーザー向けのテクニックではありませんが、ある程度「生成AIを使うことはどんな感じか」を知っておかないと、AIから有効な回答が得られない、AIに対する誤った認識が助長される、などのリスクが生じます。

## 生成AIって何！？

ここまで生成AIの定義に触れておりません。でもこれを見ている方の大半は「何となくChatGPTみたいなアレやんな」と考えていると思います。それで大丈夫です。生成AIはエラい研究者や開発者が一概に定義したものではなく、主に開発者・利用者がじわじわと使っていった結果浸透した言葉です。2020年頃の論文を見ると生成モデルを指す場合もあったようですが。

うだうだ言ってないで野村総合研究所の定義を掲載します。すみませんでした。
> 生成AI（または生成系AI）とは、「Generative AI：ジェネレーティブAI」とも呼ばれ、さまざまなコンテンツを生成できるAIのことです。従来のAIが決められた行為の自動化が目的であるのに対し、生成AIはデータのパターンや関係を学習し、新しいコンテンツを生成することを目的としています。
参考：[野村総合研究所 生成AI](https://www.nri.com/jp/knowledge/glossary/lst/sa/generative_ai)

ジェネラティブAI警察に怒られそうな定義ですが、おおむねこの通りです。大切な以下の2点も添えておきます。

1. 出力された生成物が人間の創作物と遜色ないクオリティであったこと
2. 自然言語を用いてAIに指示できるようになったこと

今までもAI技術がバンバン使われてきました。Google検索にもAmazonのおすすめにも使われています。私たちユーザーはその恩恵をいつの間にか受けてきました。しかし生成AIはその恩恵をいつの間にかではなく正面から享受するAIです。なぜなら文章を入れるだけで別の文章が生成されるAIを、誰でも利用できるようになったからです。平たく言えばChatGPTの登場です。そこに、従来のAIとの違い、いま世間を賑わせている理由があります。


P4Usでは特にテキスト生成AIサービスをまとめて「生成AI」と呼びます。以下、一例です。

* [ChatGPT](https://chat.openai.com/ "ChatGPT") 
  * OpenAIが開発・提供する生成AI
* [Copilot](https://copilot.microsoft.com/ "Copilot")
  * Microsoftが開発・提供する生成AI / OpenAIが開発したAIを利用
* [Bard](https://bard.google.com/chat "Bard")
  * Googleが開発・提供する生成AI
* [Claude](https://claude.ai/ "Claude")
  * Anthropicが開発・提供する生成AI

...その他たくさん！好きなものを使ってね！


生成AIの技術仕様や「いや何で文章なんか生成できんねん」的な鋭い質問は書籍に譲ります。ごめんなさい。こちらから購入してください。


## やってみよう

<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../links/">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">link</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">リンク集</p>
        <p class="para card-text mb-0">生成AIに関するWebページ/書籍を紹介</p>
      </div>
    </div>
  </a>
</div>

</div>


## P4Usの作成者

作成者のresearchmapはこちら。
元大学職員で、今は大学職員風味の何かです。AIの研究者ではありません。