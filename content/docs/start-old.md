---
weight: 1
title: "はじめての方へ"
description: "ここからはじめる"
icon: Start
date: "2024-01-15T21:37:31+09:00"
lastmod: "2024-01-15T21:37:31+09:00"
draft: true
toc: true
---

{{% alert icon="🌱" context="success" %}}
**Prompt Guide for University staff(P4Us)は大学職員が生成AI利用の文化を理解し、プロンプトを学ぶためのプロンプトガイドです。**   
「固すぎず柔らかすぎない」「難しすぎず易しすぎない」情報整備を心がけます  

##### 📌 Pick up：

<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../archive/was2023/">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Emoji_Objects</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">講演(WAS2023)</p>
        <p class="para card-text mb-0">大学業務における生成AI利用の体系</p>
      </div>
    </div>
  </a>
</div>

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../basic/greeting/">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Waving_Hand</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">まずは簡単なあいさつ</p>
        <p class="para card-text mb-0">生成AIにプロンプトを入力してみよう</p>
      </div>
    </div>
  </a>
</div>

</div>
{{% /alert %}}
<br>
  
## 🔰 P4Usの使い方
---
### - プロンプトを生成AIに入力する

**プロンプト**はコンピュータ画面に対して指示を出すこと、促すことを指す言葉です。  
転じて生成AI利用の文脈では、**生成AIに対する指示文・命令文の総称**として使用されています。  
(P4Usが取り扱う生成AIの意味は本ページ後半で説明します)

P4Usでは各ページにプロンプトが掲載されており、その全てが簡単にコピーできるようになっています。  
右上のアイコンからコピーアイコンをクリックしてみましょう。

**利用者のプロンプト**
```
右上の「コピーアイコン」をクリックしてください。
ここに記載しているテキストがコピーされるので、
あとは貼り付けるだけって寸法です。
```
**プロンプトが入力された生成AIから得られた回答(生成物)**
{{% alert icon="🤖" context="success" %}}
右上の「コピー」アイコンをクリックすると、ここに記載されているテキストがコピーされます。その後、必要な場所に貼り付けてください。
{{% /alert %}}

コピーしたプロンプトは実際にChatGPTやCopilot等の生成AIに入力できるものです。  
参考として生成AIから得られた回答(生成物)も記載していますが、必ずこの回答が返ってくるとは限りません。
- **利用者自身が実際に入力してみることを強く推奨します**
- **生成AIを利用するためのアカウント登録等の手続きは取り扱っておりません**

<br>

### - プロンプトを参照する
**それなり**に、様々なプロンプトを用意しています。
- 各所から収集したプロンプト
- 運営者が日々使っているプロンプト
- 運営者が生成AIに関する講演の中で使用したプロンプト
- 運営者がワークショップ参加者より収集したプロンプト

現時点で何百ものプロンプトがあるわけではありません。  
掲載するプロンプトの数は増やし続ける方針ですが、  

- **まずは一つ一つのプロンプトの意味や目的が分かるように、できる限りていねいな説明を重視しています**
- **上級者向けのプロンプトや複雑すぎるプロンプトは掲載していません**


<br>

### - 生成AIとの付き合い方を知る
生成AIは2023年時点の流行語である一方、インターネットと同様に発展・普及が見込まれているAI技術です。  
今後は生成AIとの正しい付き合い方、ちょうどいい付き合い方を知ることがとても大切だと考えられます。

{{< alert icon="👇" context="info" text="緑色太字は別ページに飛ぶリンクです🔗" />}}

❓ 生成AIを全く使ったことが無く、プロンプトの書き方が分からない  
🔜 [まずは簡単なあいさつ]({{% relref "/docs/basic/greeting.md" %}}) 

❓ 生成AIを使うときの注意事項を知りたい  
🔜 [生成AIの限界と課題]({{% relref "/docs/essence/risk-management.md" %}})  

❓ もっと生成AIを使いこなして回答の精度を上げたい  
🔜 [回答を再帰的に改善させる]({{% relref "/docs/intermediate/self-refine.md" %}})

❓ 他のツールを連携した生成AIのイメージを知りたい  
🔜 [生成AIとツールの連携]({{% relref "/docs/essence/external-tools.md" %}})  

❓ 生成AIを使う・学ぶ上で参考になるWebページは書籍を知りたい  
🔜 [リンク集]({{% relref "/docs/links" %}})


<br>

### - できること・できないこと

❌ AI技術の基本を体系的に理解する  
⭕ <strong>アプリ・サービスとして公開されているサービスを使ってみる  </strong>


❌ AI研究の知見や最新動向を理解する  
⭕ <strong>生成AI利用の最低限の姿勢・リテラシーを身に付ける  </strong>

❌ プロンプトエンジニアリングの最新動向を理解する  
⭕ <strong>それなりに良いプロンプトの在り方を理解する  </strong>

<br>

## 🚀 P4Us案内
---
ピックアップしたページを紹介します。  
全てを確認したい人は[トップページ]({{% relref "/docs/" %}})をご覧ください。

##### - 生成AIハンズオン向けコンテンツ
<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../essence/">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Eco</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">プロンプト一歩前</p>
        <p class="para card-text mb-0">プロンプトの前提を把握する</p>
      </div>
    </div>
  </a>
</div>

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../basic/">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Potted_Plant</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">プロンプトガイド基本編</p>
        <p class="para card-text mb-0">生成AIを使ってみる</p>
      </div>
    </div>
  </a>
</div>

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../intermediate/">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Nature</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">プロンプトガイド応用編</p>
        <p class="para card-text mb-0">生成AIをもっと使ってみる</p>
      </div>
    </div>
  </a>
</div>

</div>

##### - プロンプト集

<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../links/">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Nature_People</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">プロンプト事例集</p>
        <p class="para card-text mb-0">生成AIを使いこなす</p>
      </div>
    </div>
  </a>
</div>

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../links/">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Archive</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">アーカイブ資料室</p>
        <p class="para card-text mb-0">過去の講演のプロンプトを参照する</p>
      </div>
    </div>
  </a>
</div>

</div>


##### - その他コンテンツ

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

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../support/">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Contact_Support</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">お問い合わせ先</p>
        <p class="para card-text mb-0">お問い合わせ・ご相談はお気軽にどうぞ</p>
      </div>
    </div>
  </a>
</div>


</div>


## 🤖 P4Usが扱う「生成AI」とは何か
---
ここまで生成AIの定義に触れておりません。でもこれを見ている方の大半は「何となくChatGPTみたいなアレやんな」と考えていると思います。基本的にはそれで大丈夫です。生成AIはエラい研究者や開発者が一概に定義したものではなく、主に開発者・利用者がじわじわと使っていった結果浸透した言葉です。  2020年頃の論文を見ると生成モデルを指す場合もあったようですが。

一応、P4Usが扱う生成AIの定義(意味の範囲)を簡単に説明します。

まず野村総合研究所の定義を参照しましょう。
{{% alert icon="📖" context="light" %}}
生成AI（または生成系AI）とは、「Generative AI：ジェネレーティブAI」とも呼ばれ、さまざまなコンテンツを生成できるAIのことです。従来のAIが決められた行為の自動化が目的であるのに対し、生成AIはデータのパターンや関係を学習し、新しいコンテンツを生成することを目的としています。  
参考：[野村総合研究所 生成AI](https://www.nri.com/jp/knowledge/glossary/lst/sa/generative_ai)
{{% /alert %}}

概ねその通りですが、テキストを生成するAIとして、この定義に足りない要点を加えます。

1. 自然言語を用いてAIに指示ができる
2. 出力された生成物が人間の創作物と遜色ない品質である

この要点を、ChatGPTの利用の全体像と合わせて確認しましょう。  
![ChatGPT利用の全体像](images/use_ChatGPT.png)

P4Usが想定する生成AIはこのように**利用者が入力したプロンプト(映画と劇の違いを3点に要約して)に応じた回答(1. 制作過程と技術：...)を返すために、学習済みモデル(大規模言語モデル;LLM)を活用したサービス**です。

##### よってP4Usでは大規模言語モデル(LLM)を使用したテキスト生成AIサービスをまとめて「生成AI」と呼びます。  

{{< alert context="warning" text="生成AIの技術仕様や「いや何で文章なんか生成できんねん」的な疑問の解消は関連書籍に譲ります。" />}}


<br>

## 🔍 生成AI利用の準備
---
P4Usはプロンプトを提供しますが利用者の生成AIの利用環境までは準備できません。  
以下は代表的な生成AIの一例です。無料で使える生成AIも多いので、まずはアカウントを作成しておきましょう。  

* [ChatGPT](https://chatgpt.com/ "ChatGPT") 
  * OpenAIが開発・提供する生成AI
* [Copilot](https://copilot.microsoft.com/ "Copilot")
  * Microsoftが開発・提供する生成AI / OpenAIが開発したAIを利用
* [Gemini](https://gemini.google.com/chat "gemini")
  * Googleが開発・提供する生成AI
* [Claude](https://claude.ai/ "Claude")
  * Anthropicが開発・提供する生成AI

星の数ほどあり、日々技術・インターフェースが変化し続けているので、全てを比較・説明することはできません。  
好きなものを使ってください。おすすめはChatGPTとCopilotです。  

##### ChatGPT
生成AIブームの立役者であり主人公、対話型生成AIサービスです。**「いいから登録しとけ」の筆頭。**  
複数のLLMベンチマークではほぼ負けなしのGPT-4をはじめ、無料でも汎用的かつ高速なGPT-3.5を使用できます。  
画面のシンプルさゆえに何を入力していいから分からない人が続出しています。

<br>

##### Copilot
生成AI搭載の検索エンジンです。  
GPT-4モデルを使用した検索エンジンを無料で使用できる点、検索エンジン故に回答に出典が明記される点、Edgeブラウザ(今後はWindowsOS?)との連携が極めて便利な点が強みです。

<br>


##### 組織内に導入した生成AI
P4Usでは<u>**ChatGPTやCopilotのような既存サービスだけではなく、組織内に独自に導入した生成AIの利用を支援します。**</u>  
例えばギブリーさんの[法人GAI](https://gomana.ai/product/hojin-gai/)、ユーザーローカルさんの[ユーザーローカル ChatAI](https://chat-ai.userlocal.jp/)、  
またSlackやTeamsに自前で導入するケースもあります。  
(参考： [生成AIとツールの連携]({{% relref "/docs/essence/external-tools" %}}) )


こうした生成AIは組織内文書を参照できる場合も多いです。  
しかし生成AI利用における注意点やプロンプトの考え方は共通しているため、ぜひ組織内に導入した生成AIを利用する際もご参照ください。

<br>



画面を並べればなお使いやすいと思います。

![2タブ](images/twotab.png)

<br>

## 🌱 P4Usの位置づけ 
---

生成AIの開発から利用までのフローを簡潔に示すと研究者、提供者、利用者の3者が存在します。
![p4us-position1](images/p4us-position1.PNG)

現在ある大きな問題の一つが「提供者と利用者の知識・経験のギャップ」です。
![p4us-position2](images/p4us-position2.PNG)

P4Usは利用者をサポートすることでその問題を解決する一助となることを目指します。
![p4us-position3](images/p4us-position3.PNG)


## 👾 P4Usの運営者
---
gmorikiが個人で運営しています。元大学職員で、今は大学職員風味の何かです。AIの研究者ではありません。文章下手です。
- [researchmap](https://researchmap.jp/gmoriki)

メールアドレスも公開しておりますので、相談・講演依頼、なんでもお気軽にご連絡ください！  

P4Usを作った理由やねらいは、2023年11月30日の記事をご参照ください。  
- [大学職員のためのプロンプトガイド「P4Us」を作ってしまった理由](https://note.com/pogohopper8/n/n34d3e4de7b5e)