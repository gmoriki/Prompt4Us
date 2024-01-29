---
weight: 55
title: "一言で回答の質を上げる"
description: "Zero-shot Cotを理解する"
icon: "step"
date: "2024-01-20T05:57:52+09:00"
lastmod: "2024-01-20T05:57:52+09:00"
draft: false
toc: true
---
{{< alert context="warning" text="このドキュメントは作成中です！👷" />}}

良いプロンプトには明確な指示、指示の構造化や分割、そして具体的な情報も必要です。  
そうした基本を抑えたうえで、一言で回答の質を上げるプロンプトをいくつか紹介します。  
常に有効なプロンプトである保証はありませんが、「ここまで良いプロンプトを書いたのに、肝心なところで回答がぶれる」時のような、**最後の頼みの綱**として活用ください。

Zero-shot Cotで出力の質を向上させるプロンプト

## 📃プロンプト

```
こんにちは！！今日は天気が良くて気持ちが良いです。
Take a deep breath and work on this problem step-by-step.
```
{{% alert icon="🤖" context="success" %}}
こんにちは！良い天気で気分が良い日は最高ですね。何か楽しいことをする予定がありますか？何かお手伝いできることがあれば教えてください！
{{% /alert %}}

```
こんにちは！！今日は天気が良くて気持ちが良いです。
Rephrase and expand the question and respond.
```
{{% alert icon="🤖" context="success" %}}
こんにちは！良い天気で気分が良い日は最高ですね。何か楽しいことをする予定がありますか？何かお手伝いできることがあれば教えてください！
{{% /alert %}}

```
あなたは大学教員である私とともに良質な講義をデザインする「共同デザイナー」です。
以下の条件を参考に、大学1年生向け教養科目[### 講義名 ###]の講義シラバスを作成してください。

### シラバスの要素###
* サブタイトル
* 講義概要
* 到達目標（...が理解できる、...を身に付けている、という形式で3点）
* 講義方法
    - 座学を中心とし、3回に一度はアクティブラーニングを実施予定
* 授業時間外における予・復習等の指示
* 成績評価の方法
    - 平常点、小テスト、レポート、定期試験、その他
    - 定期試験に重心を置いてください
* 参考文献
    - 「本講義に適した文献を使用」と記載してください
* オフィスアワーは水曜日13:30-14:30とする
* 講義計画
    - 講義タイトルと講義の内容、講義のねらいを明確にすること
    - 15回の講義を予定
    - 何をどのように実施するのかを、各回で明確にすること

### 講義名 ###
心理学入門

### 出力形式 ###
表形式で2つのデータを出力しなさい
## シラバス情報(サブタイトルからオフィスアワーまで)のテーブル
## 講義計画(第1回から第15回まで)のテーブル
```

{{% alert icon="🤖" context="success" %}}
以下は「心理学入門」の講義シラバスのテーブルです。最初にシラバス情報（サブタイトルからオフィスアワーまで）、次に講義計画（第1回から第15回まで）のテーブルを示します。

## シラバス情報
| サブタイトル             | 心理学入門 |
|-----------------------|------------|
| 講義概要                | この講義は心理学の基本的な概念と理論を学ぶもので、人間の心理的プロセスと行動に関する理解を深めます。心理学の歴史的背景や主要な領域についても紹介します。 |
| 到達目標                | 1. 心理学の基本的な概念や用語を理解できる。<br>2. 主要な心理学の領域や研究方法について知識を身に付けている。<br>3. 心理学的なアプローチを活用し、日常生活や他の学問領域に応用できる。 |
| 講義方法                | - 座学を中心とし、3回に一度はアクティブラーニングを実施予定 |
| 授業時間外における予・復習等の指示 | - 毎週の講義内容の復習を推奨します。<br>- 追加の読書と研究を奨励します。<br>- 質問や不明点があればオフィスアワーを活用してください。 |
| 成績評価の方法           | - 平常点、小テスト、レポート、定期試験、その他<br>- 定期試験に重点を置き、評価の基準を明確にします。 |
| 参考文献                | 本講義に適した文献を使用 |
| オフィスアワー            | 水曜日13:30-14:30 |

## 講義計画
| 回数 | 講義タイトル             | 講義の内容                                                    | 講義のねらい                                                    |
|------|-----------------------|---------------------------------------------------------------|----------------------------------------------------------------|
| 第1回 | 心理学の導入              | - 心理学の定義と歴史的背景<br>- 心理学の主要な領域            | - 心理学の基本概念を理解する<br>- 心理学の分野について知識を得る     |
| 第2回 | 研究方法と倫理規定          | - 心理学の研究方法と倫理規定<br>- 実験研究と観察研究の違い      | - 研究方法の理解と倫理的側面の認識<br>- 研究デザインに関する知識の獲得  |
| 第3回 | 生物学的基盤と神経科学       | - 生物学的な影響と神経系の構造<br>- ニューロンと神経伝達          | - 生物学的基盤に関する知識の獲得<br>- 脳の働きと神経科学の理解      |
| ...  | ...                   | ...                                                           | ...                                                            |
| 第15回 | 応用心理学と将来の展望        | - 応用心理学の領域とキャリアの可能性<br>- 心理学の将来の展望    | - 心理学の実用性と将来への展望を理解する<br>- キャリア選択の考察      |

このシラバスを基に、心理学入門の講義を設計し、学生に心理学の基本的な知識とスキルを提供できるように進めていくことができます。各回の詳細な内容や教材は、講義の進行に合わせて具体的に決定してください。
{{% /alert %}}

```
あなたは大学教員である私とともに良質な講義をデザインする「共同デザイナー」です。
以下の条件を参考に、大学1年生向け教養科目[### 講義名 ###]の講義シラバスを作成してください。

### シラバスの要素###
* サブタイトル
* 講義概要
* 到達目標（...が理解できる、...を身に付けている、という形式で3点）
* 講義方法
    - 座学を中心とし、3回に一度はアクティブラーニングを実施予定
* 授業時間外における予・復習等の指示
* 成績評価の方法
    - 平常点、小テスト、レポート、定期試験、その他
    - 定期試験に重心を置いてください
* 参考文献
    - 「本講義に適した文献を使用」と記載してください
* オフィスアワーは水曜日13:30-14:30とする
* 講義計画
    - 講義タイトルと講義の内容、講義のねらいを明確にすること
    - 15回の講義を予定
    - 何をどのように実施するのかを、各回で明確にすること

### 講義名 ###
心理学入門

### 出力形式 ###
表形式で2つのデータを出力しなさい
## シラバス情報(サブタイトルからオフィスアワーまで)のテーブル
## 講義計画(第1回から第15回まで)のテーブル

let's think step by step
```

{{% alert icon="🤖" context="success" %}}
以下は、心理学入門の講義シラバスと講義計画のテーブルです。まずはシラバス情報のテーブルを作成しましょう。

**シラバス情報**

| サブタイトル               | 心理学入門                     |
|-------------------------|-------------------------------|
| 講義概要                   | この講義は心理学の基本的な概念と原理を学ぶものであり、心理学の基礎知識を提供します。心の仕組み、行動、感情などに関する理解を深め、応用能力を高めます。   |
| 到達目標                   | 1. 心理学の主要な概念と用語を理解できる。<br>2. 心理学の研究方法とアプローチを理解し、批判的に考える能力を身に付けている。<br>3. 心理学の知識を実生活に適用し、問題解決能力を高めている。 |
| 講義方法                   | 座学を中心に採用し、3回に一度はアクティブラーニングを実施予定。 |
| 授業時間外の指示             | 毎週の授業内容の復習を推奨し、追加の読書と問題集の解答を行うことを勧めます。 |
| 成績評価の方法              | 平常点、小テスト、レポート、定期試験、その他の評価を行いますが、定期試験に重点を置きます。 |
| 参考文献                   | 本講義に適した文献を使用。詳細はシラバス内で指示します。 |
| オフィスアワー                | 水曜日13:30-14:30にオフィスアワーを設けます。 |

次に、講義計画のテーブルを作成しましょう。

**講義計画**

| 回数 | 講義タイトル           | 講義の内容                                               | 講義のねらい                                     |
|----|---------------------|-----------------------------------------------------|---------------------------------------------|
| 1  | 心理学の基本概念        | - 心理学の定義と歴史<br>- 心の仕組み<br>- 研究方法の紹介 | 心理学の基本概念を理解する                    |
| 2  | 知覚と感覚             | - 知覚のプロセス<br>- 感覚器官とその機能<br>- 視覚と聴覚   | 知覚と感覚に関する理解を深める                |
| 3  | 学習と記憶             | - 学習の種類とプロセス<br>- 記憶の仕組みと障害          | 学習と記憶の原理を理解する                    |
| 4  | 発達心理学             | - 発達段階と発達課題<br>- 発達障害と対処法             | 人間の発達過程を理解し、発達に関する知識を得る     |
| 5  | 社会心理学             | - 社会的影響と行動<br>- グループダイナミクス           | 社会心理学の基本的な概念を学ぶ                |
| 6  | 個体差と人格心理学        | - 個体差の要因と性格理論<br>- 人格の評価方法           | 個人差と人格に関する理解を深める              |
| 7  | 心理療法と臨床心理学     | - 心理療法のアプローチ<br>- 心の健康と障害           | 心理療法と臨床心理学の基本を理解する           |
| 8  | ストレスと心の健康        | - ストレスの原因と影響<br>- ストレス管理の方法        | ストレスと心の健康に関する知識を得る            |
| 9  | 心理学の応用分野         | - 応用心理学の領域紹介<br>- 職業心理学と教育心理学      | 心理学の実務への応用について理解を深める          |
| 10 | 精神障害と治療           | - 精神障害の種類と症状<br>- 精神障害の治療法          | 精神障害と治療に関する知識を習得する           |
| 11 | ユースケースと実例の検討  | - 実際の心理学のケーススタディ<br>- 応用演習          | 理論を実務に応用するスキルを養う               |
| 12 | 倫理と心理学の倫理規定     | - 心理学の倫理規定と倫理的問題の解決              | 倫理的な視点から心理学の実践を理解する           |
| 13 | 現代の心理学のトピックス   | - 現代の研究トピックス紹介<br>- 専門家のゲストスピーカー  | 最新の心理学トピックについて学ぶ               |
| 14 | 心理学のキャリアパスと展望 | - 心理学のキャリアオプション<br>- 研究とキャリアの選択   | 心理学のキャリアパスについて考える             |
| 15 | 最終試験と振り返り        | - 全学期の復習<br>- 成果の振り返りとフィードバック     | 学習成果を振り返り、講義の総括を行う            |

このような講義シラバスと講義計画を基に、心理学入門の講義をデザインすることができます。各回の講義内容とねらいを明確にし、学生が心理学の基本的な知識とスキルを習得できるように工夫されています。
{{% /alert %}}



## 📚 参考文献

[各種Prompt Engineeringの日本語実例集（Zero-CoT、mock、ReAct、ToT、Metacog、Step Back、IEPなど）](https://qiita.com/YutaroOgawa2/items/aca32f8fd7d551596cf8#05-zero-shot-cot-step-by-step)

[Large Language Models are Zero-Shot Reasoners](https://arxiv.org/abs/2205.11916)

https://arxiv.org/abs/2311.04205