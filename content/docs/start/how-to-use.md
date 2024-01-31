---
weight: 11
title: "P4Usの使い方"
description: "取扱説明書を読む"
icon: "Temp_Preferences_Eco"
date: "2024-01-30T14:12:11+09:00"
lastmod: "2024-01-30T14:12:11+09:00"
draft: false
toc: true
---


{{% alert icon="🌱" context="success" %}}
**Prompt Guide for University staff(P4Us)は大学職員が生成AI利用の文化を理解し、プロンプトを学ぶためのプロンプトガイドです。**   
「固すぎず柔らかすぎない」「難しすぎず易しすぎない」情報整備を心がけます  

##### 📌 Pick up：

<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../../archive/was2023/">
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
  <a class="text-decoration-none text-reset" href="../../basic/greeting/">
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
  
## 🔰 取扱説明書
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

{{< alert icon="" context="warning" text="プロンプト事例集や応用編は現在作成中です。ページが空でもお許しください。" />}}


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

## 🔭 プロンプトガイドの構成
---
ピックアップしたページを紹介します。  
全てを確認したい人は[トップページ]({{% relref "/docs/" %}})をご覧ください。

### - 生成AIハンズオン向けコンテンツ
<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../../essence/">
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
  <a class="text-decoration-none text-reset" href="../../basic/">
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
  <a class="text-decoration-none text-reset" href="../../intermediate/">
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

### - プロンプト集

<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../../cases/">
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
  <a class="text-decoration-none text-reset" href="../../archive/">
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


### - その他コンテンツ

<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../../links/">
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
  <a class="text-decoration-none text-reset" href="../../support/">
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

## 🌱 P4Usの位置づけ 
---

生成AIの開発から利用までのフローを簡潔に示すと研究者、提供者、利用者の3者が存在します。  

![p4us-position1](images/p4us-position1.PNG)

生成AI利用に見られる問題の一つが「提供者と利用者の知識・経験のギャップ」です。  

![p4us-position2](images/p4us-position2.PNG)

P4Usは利用者をサポートすることでその問題を解決する一助となることを目指します。  

![p4us-position3](images/p4us-position3.PNG)


## 👾 運営者
---
gmorikiが個人で運営しています。元大学職員で、今は大学職員風味の何かです。AIの研究者ではありません。文章下手です。
- [researchmap](https://researchmap.jp/gmoriki)

メールアドレスも公開しておりますので、相談・講演依頼、なんでもお気軽にご連絡ください！  

P4Usを作った理由やねらいは、2023年11月30日の記事をご参照ください。  
- [大学職員のためのプロンプトガイド「P4Us」を作ってしまった理由](https://note.com/pogohopper8/n/n34d3e4de7b5e)