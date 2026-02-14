---
weight: 61
title: "文書を作成する"
description: "告知文・企画書・議事録・引継書・報告書"
icon: "Edit_Document"
lastmod: "2026-02-14T00:00:00+09:00"
date: "2024-01-21T19:40:05+09:00"
draft: false
toc: true
---


{{< table "table-responsive" >}}
| 日時 | 使用した生成AI |
|----------|--------------|
| 2024/7/7 | ChatGPT,<br>Claude,<br>Copilot |
| 2026/2/14 | ChatGPT,<br>Claude,<br>Gemini |
{{< /table >}}

## 告知・通知文の作成
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、学内Webシステムの機能廃止を利用者に周知する必要があるときに使うプロンプトです。急なシステム変更でも、丁寧かつ正確な告知文をすばやく作成できます。" />}}

「変更箇所」を自身の状況に合わせて変更してください。

```markdown
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

{{% alert icon="" context="light" %}}
以下の出力例は実際のAI出力を編集・整形したものです。同じプロンプトでも、使用するツールや時期によって結果は異なります。
{{% /alert %}}

{{% alert icon="🤖" context="success" %}}
**出力例**

[WebシステムA]をいつもご利用いただき、誠にありがとうございます。この度、システムの運用に関する重要なお知らせがございます。

2023年12月24日をもって、本システム内の「XXX」項目にある「YYY」機能の提供を終了させていただくこととなりました。これは、本機能が依存している学術論文データベース[DB-W]のSOAP APIが同年12月31日でサービス終了となり、新たにREST APIへと移行されるためです。

皆さまには、ご利用いただいている機能の一部を終了させる形となり、大変ご迷惑をお掛けいたしますが、今後とも[WebシステムA]を宜しくお願い申し上げます。なお、移行期間中に何かご不明な点などございましたら、お気軽にサポートまでお問合せください。
今後とも、皆さまの研究支援に努めてまいりますので、何卒ご理解とご協力を賜りますようお願い申し上げます。

{{% /alert %}}

## メール文の作成
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、他部署の担当者に仕様書の確認を依頼するメールを作成するときに使うプロンプトです。要点が伝わりやすく、受信者の負担を軽減するメール文を生成できます。" />}}

「入力」の箇所を自由に変更してください。
```markdown
あなたは情報伝達の効率化を徹底した事務職員です。
{目的}を達成するために{正しいメール文の書き方}を参照し、私が入力した文章を正しいメール文へ書き直してください。

### 目的 ###
* 多くの受信者の以下の業務負担の削減・軽減につながる。
* メール確認に要する時間の削減
* メールを捜索する時間の削減
* 重要なメールの見落としの軽減

### 正しいメール文の書き方 ###
* 一行あたり全角で30～35文字（半角で60～70文字）程度を目安にする。
* 段落ごとに一行空け、きりのよいところで改行するなど、見やすさを工夫する。
* 宛名は「教員各位」、「教員みなさま」の宛名ではなく、できるだけ具体的に誰に何をしてほしいのかを記載すること。
* 「お世話になっています。」、「お疲れ様です。」といった挨拶文をやめる。
* 見出しを付ける。見出し例：◆お願い事項、◆納期、◆手順、◆背景、◆補足（または注意点）
* 転送時は「標記の件について、転送します」だけの本文を記載しない。

### 出力例 ###
件名：【要回答：〇月〇日〆切】 文部科学省からの調査への対応
本文：
　総務課総務係　A様　←　施設課環境保全係　B

　お願いがありましてご連絡差し上げています。

◆お願い事項
・…
・…

◆〆切
　〇月〇日（　）○○:○○まで

◆回答方法

◆背景
　・…
　・…

### 入力 ###
* XX室森木から総務部のAさんへ
* 仕様書の確認の催促
* 10/31までに確認してほしい
* wordの校閲機能を使ってコメントを入れてほしい

### 出力 ###
このメール文は生成AIが作成しました。
生成AIが作成した文章には誤りが含まれる場合があります。
```

{{% alert icon="🤖" context="success" %}}
**出力例**

件名：【要確認：10/31〆切】仕様書の確認のお願い
本文：
　総務部　A様　←　XX室　森木

　仕様書の確認についてお願いがあり、
　ご連絡いたしました。

◆お願い事項
・添付の仕様書をご確認ください
・Wordの校閲機能を使用し、
　コメントを入れてください

◆〆切
　10月31日（木）まで

◆背景
・本仕様書は次回会議での承認に向けた
　最終確認となります

◆補足
・ご不明点がございましたら、
　XX室 森木までお問い合わせください

このメール文は生成AIが作成しました。
生成AIが作成した文章には誤りが含まれる場合があります。
{{% /alert %}}

{{% alert icon="" context="info" %}}
その他のメール作成プロンプトは[メール・コミュニケーション]({{% relref "/docs/cases/email-communication" %}})もご参照ください。
{{% /alert %}}

## 企画書の作成(IR活動)
---

{{< alert context="info" text="**対象: IR担当者**<br>**想定シーン**: 大学職員（IR担当）が、教員の研究時間を阻害する要因を分析するIR活動の企画書を作成するときに使うプロンプトです。分析の目的・手法・アウトプットの枠組みを素早く設計できます。" />}}

```markdown
あなたはInstitutional research(以下、IR)の責任者です。
※ Institutional research is research conducted within an institution of higher education to provide information which supports institutional planning, policy formation and decision making.

以下の要件に従い、まずIR活動の企画書の枠組みを設計してください。
その後、枠組みの概要を出力してください。

### 要件 ###
* 教員の研究時間を阻害する要因を特定したい。
* 分析した結果を研究力不足の改善に役立てたい。

### 出力 ###
企画書：1000文字程度
概要：200文字程度
```

{{% alert icon="🤖" context="success" %}}
**出力例**

##### 企画書：教員の研究時間阻害要因の分析

#### 1. 目的
教員が研究活動に充てる時間を阻害している要因を定量的・定性的に特定し、研究力強化に向けた改善策を提案する。

#### 2. 背景
近年、大学教員の研究時間は減少傾向にあり、文部科学省の調査でも教員の職務時間に占める研究割合の低下が報告されている。本学においても、教育・管理運営業務の増加が研究活動に影響を与えている可能性がある。

#### 3. 調査方法
- **教員アンケート調査**: 全教員を対象に、週あたりの業務時間配分、研究阻害要因の自己評価を実施
- **業務ログ分析**: 会議出席回数、委員会所属数、授業コマ数等の定量データを収集
- **ヒアリング調査**: 各学部から代表教員を選出し、半構造化インタビューを実施

#### 4. 分析指標
研究時間比率、会議参加時間、事務作業時間、教育準備時間

#### 5. スケジュール
4月：調査設計 → 5月：アンケート実施 → 6月：データ分析 → 7月：報告書作成

---

**概要**: 本企画は、教員の研究時間を阻害する要因をアンケート・業務ログ・ヒアリングの3手法で多角的に分析するIR活動である。定量・定性データに基づき、研究力強化に向けた具体的改善策を経営層に提案することを目的とする。
{{% /alert %}}


## 企画書の作成
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、大学DX推進のための研修プログラムの企画書を英文で作成するときに使うプロンプトです。海外の連携先への共有や、英語での提案書が必要な場面で活用できます。" />}}

「project_details」「target_audience」「objectives」の箇所を自由に変更してください。
```markdown
You are tasked with creating a comprehensive project proposal in Markdown format. This proposal will be based on the information provided in the input variables. Follow these instructions carefully to produce a well-structured and informative document.

First, you will receive the following input variables:

<project_details>
The project aims to develop a training program for university staff to enhance their skills in digital transformation (DX). The program will include workshops, online courses, and hands-on projects. Key features include collaboration with industry experts, access to advanced software tools, and ongoing support for participants. The project will require a budget of $200,000, and the timeline spans six months, starting from September 2024.

Background: With the increasing need for digital transformation in higher education, there is a significant gap in the skills required to implement effective DX strategies. This project aims to bridge that gap by providing targeted training to university staff.

Methodology: The program will follow a blended learning approach, combining online modules with in-person workshops. Participants will work on real-world projects to apply their learning and receive feedback from industry experts.

Key Features: Collaboration with tech companies, access to the latest DX tools, and personalized coaching sessions.

Resources Required: Budget of $200,000, training materials, software licenses, and expert consultants.

Milestones: Project kickoff in September 2024, first workshop in October 2024, mid-project review in December 2024, final project presentations in February 2025, and project completion in March 2025.
</project_details>

<target_audience>
The target audience for this project includes university administrators, IT staff, and faculty members who are involved in the planning and implementation of digital transformation initiatives.
</target_audience>

<objectives>
- To enhance the digital transformation skills of university staff.
- To provide hands-on experience with the latest DX tools and methodologies.
- To foster collaboration between university staff and industry experts.
- To support the successful implementation of DX strategies in higher education institutions.
</objectives>

Remember to use proper Markdown syntax throughout the document, including headers, lists, and emphasis where appropriate.

Follow these steps to create the project proposal:

1. Start with a title using a level 1 header (#):
   # University Staff DX Training Program Project Proposal

2. Add a brief project overview using a level 2 header (##):
   ## Project Overview
   The project aims to develop a training program for university staff to enhance their skills in digital transformation (DX). The program will include workshops, online courses, and hands-on projects. Key features include collaboration with industry experts, access to advanced software tools, and ongoing support for participants.

3. Describe the target audience using a level 2 header:
   ## Target Audience
   The target audience for this project includes university administrators, IT staff, and faculty members who are involved in the planning and implementation of digital transformation initiatives.

4. List the objectives using a level 2 header:
   ## Objectives
   - To enhance the digital transformation skills of university staff.
   - To provide hands-on experience with the latest DX tools and methodologies.
   - To foster collaboration between university staff and industry experts.
   - To support the successful implementation of DX strategies in higher education institutions.

5. Provide detailed project information using a level 2 header:
   ## Project Details
   ### Background
   With the increasing need for digital transformation in higher education, there is a significant gap in the skills required to implement effective DX strategies. This project aims to bridge that gap by providing targeted training to university staff.

   ### Methodology
   The program will follow a blended learning approach, combining online modules with in-person workshops. Participants will work on real-world projects to apply their learning and receive feedback from industry experts.

   ### Key Features
   - Collaboration with tech companies
   - Access to the latest DX tools
   - Personalized coaching sessions

   ### Resources Required
   - Budget of $200,000
   - Training materials
   - Software licenses
   - Expert consultants

6. Create a timeline section using a level 2 header:
   ## Timeline
   - Project kickoff in September 2024
   - First workshop in October 2024
   - Mid-project review in December 2024
   - Final project presentations in February 2025
   - Project completion in March 2025

7. Include a budget section using a level 2 header:
   ## Budget
   The project will require a budget of $200,000.

8. Describe the expected outcomes using a level 2 header:
   ## Expected Outcomes
   - Enhanced digital transformation skills among university staff.
   - Practical experience with cutting-edge DX tools and methodologies.
   - Stronger collaboration between university staff and industry experts.
   - Successful implementation of DX strategies in participating institutions.

9. Conclude the proposal with a brief summary using a level 2 header:
   ## Conclusion
   This project proposal outlines a comprehensive training program designed to equip university staff with essential digital transformation skills. By fostering collaboration with industry experts and providing hands-on experience with the latest tools, the program aims to bridge the skills gap in higher education and support the successful implementation of DX strategies.

After completing the proposal, review the document for proper Markdown formatting, ensuring all headers, lists, and emphasis are correctly applied. Make any necessary adjustments to improve readability and structure.

Present your final project proposal within <proposal> tags.

```

{{% alert icon="🤖" context="success" %}}
**出力例**

&lt;proposal&gt;

#### University Staff DX Training Program Project Proposal

##### Project Overview
The project aims to develop a training program for university staff to enhance their skills in digital transformation (DX). The program will include workshops, online courses, and hands-on projects.

##### Target Audience
University administrators, IT staff, and faculty members involved in DX initiatives.

##### Objectives
- Enhance digital transformation skills of university staff
- Provide hands-on experience with the latest DX tools
- Foster collaboration between university staff and industry experts

##### Timeline
| Milestone | Date |
|-----------|------|
| Project kickoff | September 2024 |
| First workshop | October 2024 |
| Mid-project review | December 2024 |
| Final presentations | February 2025 |
| Project completion | March 2025 |

##### Budget
Total: $200,000

&lt;/proposal&gt;

{{% /alert %}}

## 議事録の作成
---

議事録の作成に関するプロンプトは[会議・議事録]({{% relref "/docs/cases/meeting-minutes" %}})にまとめています。

## 引き継ぎ書の作成
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、異動や退職に伴い後任者向けの引き継ぎ書を作成するときに使うプロンプトです。業務内容・連絡先・注意事項を網羅したドキュメントを漏れなく作成できます。" />}}

「current_role」「tasks」「important_information」の箇所を自由に変更してください。
```markdown
You are tasked with creating a comprehensive handover document in markdown format for a job transition. This document will help ensure a smooth transfer of responsibilities and knowledge to the person taking over your role. Follow these instructions carefully to create an effective handover document.

First, you will be provided with three pieces of information:
1. Your current role:
<current_role>
データに関する収集・調査対応
</current_role>

2. A list of your main tasks and responsibilities:
<tasks>
* 他部署から依頼を受けたデータの提供
* 研究データ分析および分析・可視化した結果の提供
* 適切なデータマネジメント
</tasks>

3. Important information, contacts, and resources:
<important_information>
* 理事および会議に基づき実行すること
* データ規約に則りデータの提供を行うこと
* ベンダーと協力し、データベースの保守を怠らないこと
</important_information>

Using this information, create a detailed handover document in markdown format. Include the following sections:
1. Introduction
   - Brief explanation of the document's purpose
   - Your current role and the date of the handover
2. Role Overview
   - Detailed description of your current role
   - Key responsibilities and objectives
3. Tasks and Responsibilities
   - List of main tasks, broken down into subsections if necessary
   - Step-by-step procedures for critical tasks
   - Frequency or deadlines for recurring tasks
4. Important Contacts
   - List of key people, their roles, and contact information
   - Include internal and external contacts
5. Resources and Tools
   - Software, systems, and tools used in the role
   - Access information (where appropriate) or instructions on how to gain access
   - Links to important documents, shared drives, or repositories
6. Ongoing Projects
   - List of current projects and their status
   - Key deadlines and milestones
   - Any critical information or challenges
7. Tips and Best Practices
   - Your insights and advice for succeeding in the role
   - Common pitfalls to avoid
8. Transition Plan
   - Suggested timeline for knowledge transfer
   - Any scheduled handover meetings or training sessions

Follow these formatting guidelines:
- Use appropriate markdown syntax for headers, lists, and emphasis
- Use level 1 headers (#) for main sections and level 2 headers (##) for subsections
- Use bullet points (-) for lists
- Use bold (**) for emphasis on important points
- Include a table of contents at the beginning of the document
After creating the document, review it to ensure all critical information is included and properly formatted. Your final output should be a complete, well-structured markdown document that will serve as an effective handover guide for your successor.
Write your complete handover document inside <handover_document> tags.
```

{{% alert icon="🤖" context="success" %}}
**出力例**

&lt;handover_document&gt;

#### 引き継ぎ書：データに関する収集・調査対応

##### 目次
1. はじめに
2. 業務概要
3. 主要業務と手順
4. 重要な連絡先
5. 使用ツール・リソース
6. 進行中のプロジェクト
7. Tips・注意事項
8. 引き継ぎスケジュール

##### 1. はじめに
本書は「データに関する収集・調査対応」業務の引き継ぎ資料です。

##### 2. 業務概要
- 他部署からの依頼に基づくデータ提供
- 研究データの分析・可視化
- データベースの保守・管理

##### 3. 主要業務と手順
###### 3-1. データ提供
1. 依頼メールを受領
2. **データ規約**に基づき提供可否を判断
3. 承認後、データを抽出・加工して提供

...（以下略）

&lt;/handover_document&gt;
{{% /alert %}}


## 文章を校正する
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員や大学教員が、作成した日本語文書の読みやすさや文法の正確さをチェックしたいときに使うプロンプトです。報告書・申請書・メールなど、公式文書の品質を向上させるのに役立ちます。" />}}

日本語の文章を生成AIに校正してもらうプロンプトです。
英語でルールを記述しているのは、日本語の文法規則を生成AIに正確に伝えるためです。以下のプロンプトをコピーし、末尾の「Text」以降に校正したい文章を入力してください。

```markdown
Your task is to review and refine a Japanese article, focusing on correcting and improving the use of conjunctions and adverbs.

#### Rules
Ensure that your corrections and suggestions are accurate and natural-sounding in Japanese. Check for grammatical errors, inconsistencies, and unclear expressions. Provide clear and concise feedback, highlighting specific areas of improvement and suggesting alternative phrases or sentences where necessary. You MUST prioritize clarity and coherence in your revisions.

### Advanced Rules
the four principles for determining the order of modifiers of Japanese:
1. Place clauses before phrases.
2. Place longer modifiers earlier, and shorter ones later.
3. Place broader contexts and more important information earlier.
4. Rearrange based on the degree of affinity (familiarity) with the content.
the principles for using commas (、) in Japanese:
1. When there are two or more long modifiers, place a comma at their boundaries.
2. Place a comma when the natural order of words is reversed.

### Text
```

このプロンプトに含まれるAdvanced Rulesは、日本語の文章を読みやすくするための基本原則です。

**修飾語の語順4原則**（長い修飾語ほど前に、短い修飾語ほど後に配置する等のルール）:
1. 句よりも節を前に置く
2. 長い修飾語を前に、短い修飾語を後に置く
3. より広い文脈や重要な情報を前に置く
4. 内容との親和性（なじみやすさ）に応じて並べ替える

**読点の原則**（読みやすさのために読点「、」を打つ位置のルール）:
1. 長い修飾語が2つ以上あるとき、その境界に読点を打つ
2. 語順が通常と逆になっているとき、読点を打つ

{{% alert icon="🤖" context="success" %}}
**出力例**

**校正結果：**

**修正前：** 本学における教育研究活動についての今後のあり方に関する中長期的な検討を行うことを主な目的として設置された委員会においてこの件を議論した。

**修正後：** 本学における教育研究活動の今後のあり方を中長期的に検討するために設置された委員会において、この件を議論した。

**修正箇所と理由：**
- 「についての〜に関する」：修飾の重複を整理し、簡潔にしました
- 「委員会において」の後に読点を追加：長い主語の後に読点を置くことで読みやすくしました（読点の原則1）
- 修飾語の語順を整理：長い修飾語（設置目的の説明）を前に配置しました（修飾語の原則2）
{{% /alert %}}


## AIとの対話を文書化する
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、AIとやり取りしながら検討した内容を、上司や同僚に共有するための文書にまとめたいときに使うプロンプトです。議論の過程と結論を整理し、記録として残せます。" />}}

```markdown
ここまでの議論をドキュメント化してください。

### 要件 ###
* 利用者とAIのやり取りをステップごとに明確にする
* 見出しを3つつけて、キーワードを太字で示す
* 議論の結果として得られた内容を簡潔に説明
```

{{% alert icon="🤖" context="success" %}}
**出力例**

#### AIとの対話記録：学内アンケート設計の検討

##### 1. 課題の整理
利用者から「学生満足度調査のアンケート項目を見直したい」という相談があり、現行のアンケートの課題点を整理しました。主な課題は**回答率の低さ**と**自由記述の分析が困難**であることでした。

##### 2. 改善案の検討
AIから提案した改善案として、**5件法によるリッカート尺度の導入**と**設問数の削減**（30問から15問へ）を議論しました。

##### 3. 結論と次のステップ
議論の結果、次年度のアンケートでは**設問を15問に絞り、各項目に5段階評価を採用**する方向で進めることとなりました。次のステップとして、素案を教務委員会に提出します。
{{% /alert %}}

## 報告書・稟議書を作成する
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、上司に予算要求の稟議書を提出する必要があるときに使うプロンプトです。新規システム導入やイベント開催など、金額の根拠と効果を整理した稟議書を作成できます。" />}}

「変更箇所」を自身の状況に合わせて変更してください。

```markdown
あなたは大学の事務職員です。
以下の情報をもとに、上司に提出する稟議書を作成してください。

### 件名 ###
[例：学内ポータルサイトリニューアルに係る費用について]

### 要求金額 ###
[例：350万円（税込）]

### 目的・背景 ###
[例：現行の学内ポータルサイトは導入から8年が経過し、スマートフォン対応が不十分であるため、学生・教職員の利便性が低下している。リニューアルにより、情報伝達の効率化とユーザー満足度の向上を図る。]

### 期待される効果 ###
[例：
* 学生のポータル利用率の向上（現行40%→目標70%）
* 事務連絡の確認率向上
* 問い合わせ件数の削減]

### 条件 ###
* 「稟議書」のフォーマットに従う
* 金額の根拠を明示する
* 決裁区分に応じた宛先を記載する
* です・ます調で記述する
* A4用紙1枚程度にまとめる
```

{{% alert icon="🤖" context="success" %}}
**出力例**

#### 稟議書

**起案日**: 2026年2月13日
**起案者**: 情報企画課　山田太郎
**決裁者**: 事務局長

---

**件名**: 学内ポータルサイトリニューアルに係る費用について

**要求金額**: 3,500,000円（税込）

##### 1. 目的
現行の学内ポータルサイト（2018年導入）をリニューアルし、スマートフォン対応およびUI改善を行うことで、学生・教職員の利便性向上を図ります。

##### 2. 背景
- 現行システムは導入から8年が経過し、モバイル対応が不十分です
- 学生のポータル利用率は約40%にとどまっており、重要な事務連絡の見落としが発生しています

##### 3. 金額の根拠
| 項目 | 金額（税込） |
|------|-------------|
| デザイン・設計費 | 800,000円 |
| 開発・実装費 | 2,000,000円 |
| テスト・移行費 | 500,000円 |
| 初年度保守費 | 200,000円 |
| **合計** | **3,500,000円** |

##### 4. 期待される効果
- ポータル利用率の向上（40% → 70%）
- 事務連絡の確認率向上
- 窓口問い合わせ件数の削減（年間約200件減を見込む）

##### 5. スケジュール
2026年4月：業者選定 → 6月：開発着手 → 10月：リリース予定

以上、ご決裁のほどよろしくお願いいたします。
{{% /alert %}}

## 会議アジェンダを作成する
---

会議アジェンダの作成に関するプロンプトは[会議・議事録]({{% relref "/docs/cases/meeting-minutes" %}})にまとめています。

## 要望書・依頼文を作成する
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、他部署や外部機関に対して協力依頼・要望を文書で伝える必要があるときに使うプロンプトです。講演依頼・データ提供依頼・施設利用依頼など、フォーマルな依頼文を作成できます。" />}}

「変更箇所」を自身の状況に合わせて変更してください。

```markdown
あなたは大学の事務職員です。
以下の情報をもとに、依頼文（要望書）を作成してください。

### 宛先 ###
[例：○○市教育委員会 教育長]

### 差出人 ###
[例：□□大学 地域連携センター長 教授 △△△△]

### 依頼内容 ###
[例：本学が主催する地域連携シンポジウムにおいて、基調講演をお願いしたい。テーマは「地域と大学の協働による教育の未来」。日時は2026年6月15日（月）14:00〜15:00。]

### 背景・趣旨 ###
[例：本学では地域社会との連携を教育理念の柱としており、毎年シンポジウムを開催している。今年度は「教育の未来」をテーマに、自治体との協働事例を共有したい。]

### 条件 ###
* 公文書の形式に従う（文書番号・日付・宛先・差出人を明記）
* 丁寧かつ簡潔な文面とする
* 回答期限を設定する
* です・ます調で記述する
```

{{% alert icon="🤖" context="success" %}}
**出力例**

<div style="text-align: right;">□□大地連 第2026-015号</div>
<div style="text-align: right;">2026年3月1日</div>

○○市教育委員会
　教育長　殿

<div style="text-align: right;">□□大学 地域連携センター長</div>
<div style="text-align: right;">教授　△△　△△</div>

<div style="text-align: center;">**地域連携シンポジウムにおける基調講演のお願い**</div>

拝啓　時下ますますご清祥のこととお慶び申し上げます。平素より本学の教育研究活動にご理解とご協力を賜り、厚く御礼申し上げます。

さて、本学では地域社会との連携を教育理念の柱に据え、毎年「地域連携シンポジウム」を開催しております。本年度は「地域と大学の協働による教育の未来」をテーマに、下記の通り開催を予定しております。

つきましては、ご多忙のところ恐縮ではございますが、基調講演をお引き受けいただけますようお願い申し上げます。

敬具

**記**

1. **行事名**: 第10回 □□大学 地域連携シンポジウム
2. **日時**: 2026年6月15日（月）14:00〜15:00（基調講演）
3. **会場**: □□大学 中央講堂
4. **講演テーマ**: 「地域と大学の協働による教育の未来」
5. **謝金**: 本学規程に基づきお支払いいたします

**ご回答期限**: 2026年4月15日（水）までに、下記連絡先へご回答くださいますようお願いいたします。

**連絡先**: □□大学 地域連携センター事務室
TEL: 000-000-0000 / E-mail: renkei@example.ac.jp

以上
{{% /alert %}}

## 業務手順書を作成する
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 担当者の異動や退職に備えて、日常業務の手順を文書化しておきたい。口頭で説明するように箇条書きでメモを作り、AIに手順書の形に整えてもらう。" />}}

{{< alert context="warning" text="参考: [南陽市「生成AI活用実例集（プロンプト集）」](http://www.city.nanyo.yamagata.jp/dxchosei/5793) を着想源に作成" />}}

「変更箇所」を自身の状況に合わせて変更してください。

```markdown
以下のメモをもとに、誰でも手順通りに作業できる業務手順書を作成してください。

### 条件 ###
* 各手順に通し番号をつける
* 判断が必要な箇所には「※注意」として補足を添える
* 専門用語には初出時に簡単な説明を加える
* 想定所要時間があれば各手順に記載する

### 業務の概要 ###
業務名：【変更箇所：〇〇の処理】
頻度：【変更箇所：月1回／随時 など】
担当：【変更箇所：〇〇課 〇〇係】

### メモ（手順の概要） ###
【変更箇所：箇条書きで手順を書く】
```

{{% alert icon="" context="light" %}}
以下の出力例は実際のAI出力を編集・整形したものです。同じプロンプトでも、使用するツールや時期によって結果は異なります。
{{% /alert %}}

{{% alert icon="🤖" context="success" %}}
**出力例**

（「学内メーリングリストの新規作成依頼対応」の手順書を作成した場合）

**業務手順書: 学内メーリングリストの新規作成**

| 項目 | 内容 |
|------|------|
| 業務名 | メーリングリスト新規作成対応 |
| 頻度 | 随時（依頼があり次第） |
| 担当 | 情報基盤課 システム運用係 |
| 想定所要時間 | 約15分／件 |

---

**手順**

1. **申請内容を確認する**（2分）
   - 申請フォーム（Google Forms）の回答一覧を開く
   - 申請者名・所属・リスト名・用途・メンバー一覧を確認する
   - ※注意：リスト名が既存のものと重複していないか、管理画面で事前に検索すること

2. **管理画面でリストを作成する**（5分）
   - メール管理システムにログインする
   - 「新規リスト作成」を選択し、以下を入力する
     - リスト名（例: committee-xx@example.ac.jp）
     - 表示名（例: 〇〇委員会）
     - 管理者メールアドレス（申請者のアドレス）
   - ※注意：リスト名は半角英数字・ハイフンのみ使用可

3. **メンバーを登録する**（5分）
   - 「メンバー管理」からCSV一括登録を選択
   - 申請フォームのメンバー一覧をCSV形式に整形してアップロード
   - 登録完了後、メンバー数が申請内容と一致しているか確認する

4. **申請者に完了を通知する**（3分）
   - テンプレートメール（件名:「メーリングリスト作成完了のお知らせ」）を使用
   - リストアドレス・メンバー数・利用上の注意事項を記載して送信する

5. **管理台帳を更新する**（2分）
   - 共有スプレッドシート「メーリングリスト管理台帳」に以下を記録する
     - 作成日・リスト名・管理者・メンバー数・用途

{{% /alert %}}
