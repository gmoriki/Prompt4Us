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

**Prompt Guide for University staff(P4Us)は大学職員が生成AI利用の文化を理解し、プロンプトを学ぶためのプロンプトガイドです。**「固すぎず柔らかすぎない」「難しすぎず易しすぎない」情報整備を心がけます。

{{% alert icon="📌" context="success" %}}
##### Pick up：

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


## 🔰 取扱説明書
---
P4Usではプロンプトを使い、プロンプトを知り、プロンプトを学ぶことができます。

**プロンプト**とは、コンピュータ画面に対して指示を出すこと、促すことを指す言葉です。
P4Usでは**生成AIに対する指示文・命令文の総称**として使用します。

P4Usに掲載されているプロンプトは簡単にコピーできるようになっています。試しに、下記のプロンプトをコピーしてみましょう。右上のコピーアイコンを選択すると、テキストをコピーできます。

```
右上の「コピーアイコン」をクリックしてください。
ここに記載しているテキストがコピーされるので、
生成AIに貼り付けて使用してください。
```

コピーしたプロンプトはChatGPTやCopilot等の生成AIサービスに入力できます。P4Usでは参考までに、生成物を記載することがありますが、必ずこの通りに返答されるわけではありません。

{{% alert icon="🤖" context="success" %}}
これは生成物のサンプルです。
{{% /alert %}}

### - プロンプトを参照する
様々なプロンプトを用意しています。現時点で何百ものプロンプトがあるわけではありません。掲載するプロンプトの数は増やし続ける方針ですが、  

- **まずは一つ一つのプロンプトの意味や目的が分かるように、できる限りていねいな説明を重視しています**
- **上級者向けのプロンプトや複雑すぎるプロンプトは掲載していません**

{{< alert icon="" context="warning" text="プロンプト事例集や応用編は現在作成中です。ページが空でもお許しください。" />}}


### - 生成AIとの付き合い方を知る
生成AIはインターネットのような汎用技術としての発展・普及が見込まれている技術です。今後はAI利用者が生成AIとの正しい付き合い方、ちょうどいい付き合い方を知ることがとても大切だと考えられます。

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


### - P4Usの中でできること・できないこと

❌ AI技術の基本を体系的に理解する  
⭕ <strong>アプリ・サービスとして公開されているサービスを使ってみる  </strong>


❌ AI研究の知見や最新動向を理解する  
⭕ <strong>生成AI利用の最低限の姿勢・リテラシーを身に付ける  </strong>

❌ プロンプトエンジニアリングの最新動向を理解する  
⭕ <strong>それなりに良いプロンプトの在り方を理解する  </strong>


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
        <p class="fs-5 fw-semibold card-title mb-1">リテラシー</p>
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
        <p class="fs-5 fw-semibold card-title mb-1">基本</p>
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
        <p class="fs-5 fw-semibold card-title mb-1">応用</p>
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
        <p class="fs-5 fw-semibold card-title mb-1">プロンプト集</p>
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
        <p class="fs-5 fw-semibold card-title mb-1">アーカイブ</p>
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
        <p class="fs-5 fw-semibold card-title mb-1">FAQ</p>
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
gmorikiが個人で運営しています。詳しくは[researchmap](https://researchmap.jp/gmoriki)をご覧ください。

P4Usを作った理由やねらいは、2023年11月30日の記事をご参照ください。  
- [大学職員のためのプロンプトガイド「P4Us」を作ってしまった理由](https://note.com/pogohopper8/n/n34d3e4de7b5e)