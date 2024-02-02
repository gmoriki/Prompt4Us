---
weight: 51
title: "テンプレートを使用する"
description: "深津さんのプロンプトを紹介"
icon: "Developer_Guide"
date: "2024-01-21T19:32:35+09:00"
lastmod: "2024-01-21T19:32:35+09:00"
draft: false
toc: true
---

このページから**プロンプトガイド応用編**がはじまります。

プロンプトエンジニアリングの基本原則はこちらからご覧ください。

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../../essence/basic-prompt">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Thumb_Up</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">良いプロンプトの基礎</p>
        <p class="para card-text mb-0">生成AIを上手に使うために</p>
      </div>
    </div>
  </a>
</div>

<br>

このページでも紹介しましたが、改めてプロンプトのテンプレートを紹介します。

```
# 命令書:
あなたは{プロの編集者}です。
以下の制約条件と入力文をもとに{最高の要約}を出力してください。

# 制約条件:
- 文字数は300文字程度。
- 小学生にもわかりやすく。
- 重要なキーワードを取り残さない。
- 文章を簡潔に。

# 入力文：
{入力文章}

# 出力文：
```

THE GUILD深津さんが公表しているプロンプトテンプレートです。  
困ったときはこの通りに従うとそこそこ良い回答を見込めます。  
ぜひテンプレートを改善したり自分の手でテンプレートを作ったりしてみてください。


## 参考
https://youtu.be/ReoJcerYtuI  
https://bocek.co.jp/media/exercise/chatgpt/3713/