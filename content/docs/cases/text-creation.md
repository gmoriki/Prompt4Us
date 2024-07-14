---
weight: 61
title: "文書を作成する"
description: "メール・告知・企画書"
icon: "article"
date: "2024-01-21T19:40:05+09:00"
lastmod: "2024-01-21T19:40:05+09:00"
draft: false
toc: true
---


{{< table "table-responsive" >}}
| 日時 | 使用した生成AI | 
|----------|--------------|
| 2024/7/7 | ChatGPT(GPT-3.5),<br>Claude(3.5 Sonnet),<br>Copilot(GPT-4) |
{{< /table >}}

## 告知・通知文の作成
---

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
{{% alert icon="🤖" context="success" %}}
[WebシステムA]をいつもご利用いただき、誠にありがとうございます。この度、システムの運用に関する重要なお知らせがございます。

2023年12月24日をもって、本システム内の「XXX」項目にある「YYY」機能の提供を終了させていただくこととなりました。これは、本機能が依存している学術論文データベース[DB-W]のSOAP APIが同年12月31日でサービス終了となり、新たにREST APIへと移行されるためです。

皆さまには、ご利用いただいている機能の一部を終了させる形となり、大変ご迷惑をお掛けいたしますが、今後とも[WebシステムA]を宜しくお願い申し上げます。なお、移行期間中に何かご不明な点などございましたら、お気軽にサポートまでお問合せください。
今後とも、皆さまの研究支援に努めてまいりますので、何卒ご理解とご協力を賜りますようお願い申し上げます。

{{% /alert %}}

## メール文の作成
---

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

## 企画書の作成(IR活動)
---

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


## 企画書の作成
---

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

## 議事録の作成
---

引用元：[@00oichanさんのツイート](https://x.com/00oichan/status/1799439321713504347)
```markdown
指示：
1. 音声文字認識のテキストを読みやすい文章へ変換してください。
2. JTF日本語標準スタイルガイドに従い、文法的に正しい自然な文章に修正し、句読点を適切に追加してください。
3. 曖昧な表現や省略部分を補完し、言い直しや繰り返しを整理して冗長な部分を削除してください。
4. 話者名を明記してください。不明な場合は「ー」としてください。
5. 専門用語や固有名詞を正確に記述し、必要に応じて注釈を追加してください。
6. 数字、日付、時間を正確に記載してください。
7. 具体例やエピソードを詳細に記述し、話の主旨を明確にしてください。
8. 誤字脱字をチェックし、正しい表現に修正してください。
9. 出力時は1行辺り150文字程度で改行を入れ、1テーマあたり10-15行前後が理想です。
10. 要点を太字にしてください。
11. です ます調で書いてください。
12. 同じ人が連続で会話している場合は会話記録を1行にまとめてください。

出力言語：
日本語

処理手順：
1. プロンプト文を読み、内容を理解します。
2. テーマ一覧を作成してください。大テーマと小テーマがあるといいです。
3. テーマごとに表形式で会話の記録を書いていきます。
4. 会話のテーマが変わったら冒頭にテーマ名を書きます。
5. 各行の冒頭に話者の名前を書きます。話者が不明な場合は「ー」と書きます。
6. 1行辺り150文字程度で改行を入れます。
7. 1テーマあたり10-15行前後として次のテーマを作成する。
8. 入力文と出力分を比較し、入力文を読み飛ばしていないか確認します。
9. すべての出力が完了したら --- 完了 --- と表示してください。

出力後の過去の指摘：
1. 1行辺り150文字程度で改行を入れるルールを守れていないです。
2. 1テーマあたり10-15行前後として次のテーマを作成するというルールを守れていないです。
3. テーマが冒頭に記載されていません。会話が変わったらテーマ名を挿入してください

出力形式：表形式
### テーマ一覧
{{テーマ名を箇条書きで記載する}}
{{テーマ名を箇条書きで記載する}}
{{テーマ名を箇条書きで記載する}}

### テーマ名
| 番号 | 話者 | 読みやすい文章 |
| --- | --- | --- |
| --- | --- | --- |

### テーマ名
| 番号 | 話者 | 読みやすい文章 |
| --- | --- | --- |
| --- | --- | --- |

入力文：
（次のチャットでお伝えします。出力せずに待機してください）
```


## 引き継ぎ書の作成
---

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


## 文章を校正する
---

開発途中です。
「Text」以降に入力してください。

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


## AIとの対話を文書化する
---

```
ここまでの議論をドキュメント化してください。

### 要件 ###
* 利用者とAIのやり取りをステップごとに明確にする
* 見出しを3つつけて、キーワードを太字で示す
* 議論の結果として得られた内容を簡潔に説明
```