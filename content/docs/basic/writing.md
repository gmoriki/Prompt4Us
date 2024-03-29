---
weight: 42
title: "文章を書こう"
description: "「書き出し」タスクの体験"
icon: "Draw"
date: "2024-01-21T19:30:59+09:00"
lastmod: "2024-01-21T19:30:59+09:00"
draft: false
toc: true
---

ここでは多様なテキストやプログラムコードをまとめて「文章」と呼びます。  
生成AIは(その名の通り)文章を生成することができます。  

{{< table "table-responsive" >}}
| 日時 | このページで使用した生成AI | 
|----------|--------------|
| 2024/1/20 | ChatGPT(GPT-3.5) |
{{< /table >}}

<br>

[まずは簡単なあいさつ]({{% relref "/docs/basic/greeting.md" %}})でみたように、生成AIは利用者が入力したプロンプトに応じて回答を生成します。  

```
こんにちは！！今日は天気が良くて気持ちが良いです。
```
{{% alert icon="🤖" context="success" %}}
こんにちは！良い天気で気分が良い日は最高ですね。何か楽しいことをする予定がありますか？何かお手伝いできることがあれば教えてください！
{{% /alert %}}

もっと品質・精度が高い生成物を目指してみます。  

<br>

## 📩 メール文を作成する
---
所属する部署やメールをやり取りしている分野を入れてください。  

```
あなたは大学教務のプロフェッショナルです。
以下の要件に従い、メール文章を作成してください。

### 要件 ###
- 返信が遅れたことを詫びる
- 大学の不備により学務システムに誤りが発見された
- 原因追及を進める一方で、現場での対応を進めるため、都合が良い日時をうかがう
- 形式の{contents}を埋めてください

### 形式 ###
xxx様

お世話になっております。
九州大学の森木です。

ご連絡いただきありがとうございました。
{contents}

どうぞよろしくお願いいたします。
```

{{% alert icon="🤖" context="success" %}}
以下は、要件に従ったメールの文章です。

---

xxx様

お世話になっております。九州大学の森木です。

ご連絡いただきありがとうございました。お返事が遅くなり、申し訳ございません。

さて、大学の学務システムについて、不備が発見されましたこと、重く受け止めております。この問題について、原因追及を進めつつ、現場での対応も迅速に進めてまいります。

ご不便をおかけし、誠に申し訳ございません。都合が宜しければ、お話をお伺いし、より詳細な情報を共有させていただきたく存じます。何日何時がご都合が良いでしょうか？

ご返信いただければ幸いです。どうぞよろしくお願いいたします。

どうぞよろしくお願いいたします。

九州大学
森木
{{% /alert %}}


少し冗長な内容が含まれているので修正してみます。

```
この内容をベースに、以下の点を修正してください。

- 以下の例に従い、必ず「。」で改行してください。例だけではなく全体の文章に適用すること。
例：
before
ご連絡いただきありがとうございました。お返事が遅くなり、申し訳ございません。
after
ご連絡いただきありがとうございました。
お返事が遅くなり、申し訳ございません。

- 最後の署名は不要です
-「どうぞよろしくお願いします。」は1つだけ採用してください
```

{{% alert icon="🤖" context="success" %}}
xxx様

お世話になっております。九州大学の森木です。

ご連絡いただき、ありがとうございました。  
お返事が遅くなり、申し訳ございません。

さて、大学の学務システムについて、不備が発見されましたこと、重く受け止めております。  
この問題について、原因追及を進めつつ、現場での対応も迅速に進めてまいります。

ご不便をおかけし、誠に申し訳ございません。都合が宜しければ、お話をお伺いし、より詳細な情報を共有させていただきたく存じます。  
何日何時がご都合が良いでしょうか？

ご返信いただければ幸いです。  
どうぞよろしくお願いいたします。
{{% /alert %}}


全て指示通り、というわけにはいきませんが、メール文のひな型としては十分でしょう。  
一連の指示の中で生成物を修正しましたが、次からは一つのプロンプトで対応できるように、プロンプトも修正しておきます。  
9行-17行目に追記しています。

```markdown {linenos=inline,hl_lines=["9-17"],anchorlinenos=false}
あなたは大学教務のプロフェッショナルです。
以下の要件に従い、メール文章を作成してください。

### 要件 ###
- 返信が遅れたことを詫びる
- 大学の不備により学務システムに誤りが発見された
- 原因追及を進める一方で、現場での対応を進めるため、都合が良い日時をうかがう
- 最後の署名は不要です
-「どうぞよろしくお願いします。」は1つだけ採用してください
- 以下の例に従い、必ず「。」で改行してください。例だけではなく全体の文章に適用すること。
例：
before
ご連絡いただきありがとうございました。お返事が遅くなり、申し訳ございません。
after
ご連絡いただきありがとうございました。
お返事が遅くなり、申し訳ございません。
- 形式の{contents}を埋めてください

### 形式 ###
xxx様

お世話になっております。
九州大学の森木です。

ご連絡いただきありがとうございました。
{contents}

どうぞよろしくお願いいたします。
```
<br>


## 📢 告知文を作成する
---
システム運用者がシステム利用者向けにメンテナンスの告知文章を作成してみました。

```
あなたはWebシステム運用のスペシャリストです。
以下の文脈と要件に従って、利用者向けの告知文を作成してください。
 
### 文脈 ###
運用している[WebシステムA]の「XXX」項目内にある機能「YYY」を廃止する。
理由は、学術論文データベースである[DB-W]が今まで使用していたSOAP APIが20XX年12月31日で終了し、RESTAPIに移行するため。
よって12月24日を以って「YYY」は使用不可となる。
 
### 条件 ###
* 「[WebシステムA]をいつもご利用いただきありがとうございます。」から始める
* 最初から最後まで丁寧な言い回しを心がける
* 告知文は日本語で400文字程度とする

```
{{% alert icon="🤖" context="success" %}}
[WebシステムA]をいつもご利用いただき、誠にありがとうございます。この度、システムの運用に関する重要なお知らせがございます。

2023年12月24日をもって、本システム内の「XXX」項目にある「YYY」機能の提供を終了させていただくこととなりました。これは、本機能が依存している学術論文データベース[DB-W]のSOAP APIが同年12月31日でサービス終了となり、新たにREST APIへと移行されるためです。

皆さまには、ご利用いただいている機能の一部を終了させる形となり、大変ご迷惑をお掛けいたしますが、今後とも[WebシステムA]を宜しくお願い申し上げます。なお、移行期間中に何かご不明な点などございましたら、お気軽にサポートまでお問合せください。
今後とも、皆さまの研究支援に努めてまいりますので、何卒ご理解とご協力を賜りますようお願い申し上げます。

{{% /alert %}}

## 🔄 翻訳する
---

先ほどの告知文を英語に翻訳してみます。  
(新しい会話を作成しています)

````
以下の文章を、モダリティを意識して、ネイティブスピーカーのような英語に翻訳してください

```
[WebシステムA]をいつもご利用いただき、誠にありがとうございます。この度、システムの運用に関する重要なお知らせがございます。

2023年12月24日をもって、本システム内の「XXX」項目にある「YYY」機能の提供を終了させていただくこととなりました。これは、本機能が依存している学術論文データベース[DB-W]のSOAP APIが同年12月31日でサービス終了となり、新たにREST APIへと移行されるためです。

皆さまには、ご利用いただいている機能の一部を終了させる形となり、大変ご迷惑をお掛けいたしますが、今後とも[WebシステムA]を宜しくお願い申し上げます。なお、移行期間中に何かご不明な点などございましたら、お気軽にサポートまでお問合せください。
今後とも、皆さまの研究支援に努めてまいりますので、何卒ご理解とご協力を賜りますようお願い申し上げます。
````
{{% alert icon="🤖" context="success" %}}

Thank you very much for always using [Web System A]. We have important information regarding the operation of the system.

As of December 24, 2023, we will be discontinuing the "YYY" feature in the "XXX" section of this system. This decision is due to the SOAP API of the academic paper database [DB-W], on which this feature relies, ending its service on December 31 of the same year and transitioning to a new REST API.

We understand that this may cause some inconvenience as we are discontinuing a part of the features you have been using, but we kindly ask for your understanding. We sincerely appreciate your continued use of [Web System A]. If you have any questions or concerns during the transition period, please don't hesitate to contact our support team.

We will continue to strive to support your research needs, and we kindly request your understanding and cooperation in this matter.
{{% /alert %}}
    