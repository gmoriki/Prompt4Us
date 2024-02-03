---
weight: 999
title: "職員研修@北陸大学"
description: "ハンズオンで理解する生成AI"
icon: "article"
date: "2024-02-03T20:55:25+09:00"
lastmod: "2024-02-03T20:55:25+09:00"
draft: false
toc: true
---

{{< table "table-responsive" >}}
| 日時 | このページで使用した生成AI | 
|----------|--------------|
| 2024/02/03 | ChatGPT(GPT-3.5) <br> 一部でBardやCopilotを紹介 |
{{< /table >}}
<br>


## ⚠️ 生成AIの限界と課題
---
こちらのページもご参照ください！

<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../../essence/risk-management">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Error</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">生成AIの限界と課題</p>
        <p class="para card-text mb-0">最低限、リスクを理解する</p>
      </div>
    </div>
  </a>
</div>

</div>

<br>


## 👍 適切な生成AI利用
---

あまりよくない例：
```
鎌倉幕府　いつから
```
{{% alert icon="🤖" context="success" %}}
鎌倉幕府は、日本の歴史において、1185年から1333年まで存在した武士政権です。鎌倉幕府の成立は、1185年に源頼朝が壇ノ浦の戦いで平氏を打倒し、鎌倉に幕府を開くことに始まります。この時期は鎌倉時代とも呼ばれ、鎌倉幕府は武士の政権として、日本の支配を行いました。鎌倉幕府は、鎌倉時代の終焉である1333年の建武の新政によって滅ぼされ、南北朝時代へと移行しました。
{{% /alert %}}


適切な使い方の一例：
```
鎌倉幕府が始まった年は1192年ではないのではないでしょうか。 
この仮説の妥当性を検証したいので、まずは別の仮説や考えを提示ください。
```

{{% alert icon="🤖" context="success" %}}
鎌倉幕府が1192年に始まったという通説に疑問を持って、別の仮説や考えを提示することは重要です。以下にいくつかの可能性を示します：

1. 鎌倉幕府の成立は1192年以前である可能性:
   - 仮に1192年以前に成立したと仮定するならば、鎌倉幕府が成立した具体的な日付や出来事を検証する必要があります。歴史的な文献や資料を調査して、新たな証拠や情報を見つけることが必要かもしれません。

2. 鎌倉幕府の成立は1192年以降である可能性:
   - 通説と異なる立場をとり、鎌倉幕府の成立が1192年以降に起こったという仮説を検証できます。これには、当時の歴史的な出来事や記録、関連する人物の行動を調査して、新たな視点を提供するかもしれません。

3. 鎌倉幕府の概念や性質についての異なる解釈:
   - 鎌倉幕府の成立を年数だけで考えるのではなく、その性質や概念について異なる解釈を考えることもできます。たとえば、鎌倉幕府が形式的には1192年に成立したとしても、その前後に重要な変化や準備期間があったのかもしれません。このような観点から新たな仮説を検討できます。

どの仮説を採用するかは、具体的な歴史的な証拠や研究に基づいて判断する必要があります。歴史の研究においては、異なる仮説を検証し、証拠に基づいて正確な結論を導くための綿密な調査が必要です。
{{% /alert %}}

<br>


## ⚙️ 良いプロンプトの基礎
---
こちらのページもご参照ください！

<div class="row flex-xl-wrap pb-4">

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

</div>

<br>

## 👐 ChatGPTハンズオン
---

### - 文章を要約する

テンプレートを活用

参考：[北陸大学 データサイエンス・AI教育プログラム始動](https://www.hokuriku-u.ac.jp/datascience/)

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
北陸大学は、データ分析を地域や職場で活かすことができる人材を育成する「データサイエンス・AI教育プログラム」を2022年４月から開始しました。
プログラム対象科目の授業設計や教材提供、ツール利用、講師派遣について、ビジュアル分析プラットフォーム「Tableau」を提供するTableau（本社；米国シアトル、プレジデント兼CEO：マーク・ネルソン）とデータサイエンスソフト「Exploratory」を提供するExploratory, Inc.（本社；アメリカ合衆国カリフォルニア州、CEO：西田勘一郎）と連携し、大量のデータから意味や価値を見いだす「データリテラシー」の向上を目指します。
Tableau及びExploratoryと連携した教育プログラムの実施は、中部地方の大学では初めてです。
21世紀を生きる私たちは、モノのインターネット（Internet of Things: IoT）からあふれる圧倒的な情報の洪水から、分析を通じてビッグデータを理解し活用する能力、情報の解釈と意味を見いだすことを可能にする「データリテラシー」を身につけることが求められています。
北陸大学データサイエンス・AI教育プログラムでは、正確な予測を導き、相互に繋がり合う関係性を見いだすため、全学部1年次必修の情報リテラシー科目でTableau Desktopを用いた演習を実施するとともに、経済経営学部の統計学入門科目においてはExploratoryを活用した分析を行います。また実データを用いた実践的な教育のため、株式会社太陽アソシエイツ（石川県金沢市）から分析課題で用いる店舗の販売データを提供いただき、データ分析支援企業のヴェルク株式会社（東京都千代田区、代表取締役:田向祐介）から分析結果の報告方法について指導いただきます。

# 出力文：
```

{{% alert icon="🤖" context="success" %}}
北陸大学は、2022年４月から「データサイエンス・AI教育プログラム」を開始し、地域や職場でデータ分析を活用する人材を育成します。このプログラムは、ビジュアル分析プラットフォーム「Tableau」とデータサイエンスソフト「Exploratory」の連携により、データリテラシー向上を目指します。これは中部地方の大学では初の試みです。

21世紀では、ビッグデータを理解し活用する能力が求められており、北陸大学では情報リテラシー科目でTableau Desktopを用いた演習や統計学入門科目でExploratoryを活用した分析を行います。さらに、実データを使用した実践的な教育を提供するため、株式会社太陽アソシエイツから店舗の販売データを提供し、ヴェルク株式会社から分析結果の指導を受けます。

このプログラムを通じて、学生はデータ分析に必要なスキルを習得し、ビッグデータの活用や情報の解釈能力を向上させることができます。
{{% /alert %}}

```
本質的な点、3点を箇条書きにしてください
```

{{% alert icon="🤖" context="success" %}}
1. 北陸大学の「データサイエンス・AI教育プログラム」は、2022年４月から始まり、地域や職場でデータ分析を活用する人材を育成する重要なイニシアティブです。

2. プログラムはビジュアル分析プラットフォーム「Tableau」とデータサイエンスソフト「Exploratory」の連携を通じて、データリテラシー向上を目指し、中部地方の大学では初の試みです。

3. 学生はプログラムを通じてデータ分析スキルを習得し、ビッグデータの活用能力や情報の解釈力を向上させることが期待されます。
{{% /alert %}}

<br>

### - 会話のスレッドを文書化する

```
ここまでの議論をドキュメント化してください。

### 要件 ###
* 利用者とAIのやり取りをステップごとに明確にする
* 見出しを3つつけて、キーワードを太字で示す
* 議論の結果として得られた内容を簡潔に説明
```



{{% alert icon="🤖" context="success" %}}

#### 利用者とAIのやり取り

**利用者:** AI、北陸大学の「データサイエンス・AI教育プログラム」について要約をお願いします。

**AI:** もちろんです。以下に要約いたします。

#### 議論1: プログラムの開始と目的

**利用者:** 北陸大学の「データサイエンス・AI教育プログラム」について詳しく教えてください。

**AI:** 北陸大学は2022年４月から「データサイエンス・AI教育プログラム」を開始し、地域や職場でデータ分析を活用する人材を育成します。これは、ビジュアル分析プラットフォーム「Tableau」とデータサイエンスソフト「Exploratory」の連携により、データリテラシー向上を目指す取り組みで、中部地方の大学では初めての試みです。

#### 議論2: プログラムの内容

**利用者:** プログラムの具体的な内容は何ですか？

**AI:** プログラムでは、学生は情報リテラシー科目でTableau Desktopを用いた演習や、経済経営学部の統計学入門科目でExploratoryを活用した分析を行います。実データを使用した実践的な教育も行われ、株式会社太陽アソシエイツから店舗の販売データを提供し、ヴェルク株式会社から分析結果の指導を受けます。

#### 議論3: プログラムの重要性

**利用者:** なぜこのプログラムが重要なのですか？

**AI:** このプログラムを通じて、学生はデータ分析に必要なスキルを習得し、ビッグデータの活用や情報の解釈能力を向上させることが期待されます。これは、21世紀においてビッグデータを理解し活用する能力が求められており、地域や職場でデータ分析を実施するために重要なステップです。
{{% /alert %}}

<br>


### - 施設の名前を考える

```
あなたはプロのコピーライターです。
以下の要件に適したプロダクト名を5つ挙げてください。

### 要件 ###
- 大学のキャンパスに新しく建てられたビル型施設の中にある空間です
- ビル型施設には理系の教員の研究室が多い、特に情報系教員
- 洗練されたシンプルなデザインの椅子や机が、カフェのような場所を思わせます
- 建学の精神「質実剛健」にもとづいた落ち着いた空間
- ホワイトボードやソファも充実して、学生の学びを積極的にサポートします

### 出力 ###
プロダクト名とその理由
```

{{% alert icon="🤖" context="success" %}}
以下は、要件に合ったプロダクト名とその理由です：

1. "InnoHub"（イノハブ）
   - 理系教員の研究と情報系学生の創造性を強調し、イノベーションの中心地を表現しています。

2. "Campus Oasis"（キャンパスオアシス）
   - 質実剛健な空間とカフェライクなデザインを組み合わせ、学生にとっての癒しの場所を提供します。

3. "Sci-Tech Lounge"（サイテックラウンジ）
   - 理系の教員と情報系学生のための場所で、科学と技術に関する活発な交流を促進します。

4. "Mindful Study Hub"（マインドフルスタディハブ）
   - 落ち着いた雰囲気と充実した学習環境で、学生の学びと創造力を育む場所を提供します。

5. "Academic Nexus"（アカデミックネクサス）
   - キャンパス内の学術的なつながりと交流を強調し、知識の交流の場を表現しています。

{{% /alert %}}

<br>


### - Excelの関数を作ってもらう

参考：[東京都：都職員のアイデアが詰まった文章生成AI活用事例集](https://www.digitalservice.metro.tokyo.lg.jp/documents/d/digitalservice/ai_prompt/)

```
# 指示
局内講習会の参加者リストにおける「参加可否」列に“参加”もしくは“不参加”を入
力する計算式を作成してください。

# 目的
正確な計算式をエクセルに入力し、参加者の参加可否状況を把握するため

# 情報
・参加可否の条件：
・条件：3つの参加条件（例：参加登録、参加許可、必要な情報の提出）が
全て満たされている
・シート構造：A列には参加者名、B列には参加登録状況（1で登録済み、0で未
登録）、C列には参加の許可状況（1で許可済み、0は未許可）、D列には必要
な情報の提出状況（1で提出済み、0で未提出）が記載されています。E列に関
数を入れたいです。

# ルール
・シンプルかつ理解しやすい計算式であること
```

{{% alert icon="🤖" context="success" %}}
参加可否を判断するためのシンプルで理解しやすい計算式を作成します。E列に以下の計算式を入力してください：

`=IF(AND(B2=1, C2=1, D2=1), "参加", "不参加")`

この計算式は、以下の条件を満たす場合に"参加"、それ以外の場合に"不参加"と表示します：

1. B列の値が1（登録済み）であること。
2. C列の値が1（許可済み）であること。
3. D列の値が1（提出済み）であること。

これにより、3つの条件が全て満たされている場合に"参加"と表示され、いずれかの条件が満たされていない場合に"不参加"と表示されます。
{{% /alert %}}

<br>


### - 翻訳文の作成

山田(2023)によると翻訳過程には「翻訳の製作工程」と「翻訳の後工程」があります。ここでは「翻訳の製作工程」を紹介します。  
参考：[ChatGPT翻訳術　新AI時代の超英語スキルブック](https://www.alc.co.jp/entry/7023020)

プロンプトは一部加筆したものです。

```
次の{原文}の日本語の文章を英語に翻訳してください。
1. 翻訳するときに以下の条件を満たしてください。
2. {用語集}の中の対訳を正しく使って{原文}を英語に翻訳してください。{用語集}はカンマ区切りのCSV形式になっています。


### 目的 ###
ビジネスパートナーとの円滑なコミュニケーションによる顧客満足度の向上

### 対象読者 ###
丁寧なコミュニケーションを必要とする教員
(利用システムの不備に対して怒りの感情を持っている)

### 用語集 ###
JA,EN
"架空の研究科","Faculty of NAZO"
"XYZシステム","x-y-z application"

### 原文 ###
架空の研究科
X先生

大変お世話になっております。
Y大学の佐藤です。

ご連絡いただきありがとうございました。
XYZシステムについて、ご意見いただいた内容を踏まえまして本学で検討いたします。
今しばらくお待ちいただけますと幸いです。

ご多忙のところ恐れ入りますが、
どうぞよろしくお願いいたします。

### 出力 ###
**翻訳された原文**だけを出力
```

{{% alert icon="🤖" context="success" %}}
"Faculty of NAZO" 
Professor X

Thank you very much for your kind assistance.
This is Sato from Y University.

Thank you for contacting us.
We will consider the feedback you provided regarding the XYZ System at our university.
We would appreciate your patience while we review it.

I apologize for your busy schedule, but 
thank you very much in advance.
{{% /alert %}}

参考までに、他の生成AIの回答も掲載します。  
**ChatGPT(GPT-4)**

{{% alert icon="🤖" context="success" %}}
**Translated Text:**

Faculty of NAZO
Professor X

Thank you very much for your continuous support.
I am Sato from Y University.

Thank you for getting in touch with us.
Based on the feedback you provided about the x-y-z application, we will consider it at our university.
We would appreciate your patience for a while longer.

We apologize for the inconvenience during your busy schedule,
but we kindly ask for your continued cooperation.
{{% /alert %}}

**Copilot(GPT-4)**

{{% alert icon="🤖" context="success" %}}
Faculty of NAZO
Professor X,

I hope this message finds you well.
This is Sato from Y University.

Thank you for reaching out to us.
We will consider your feedback about the x-y-z application at our university.
We would appreciate your patience in this matter.

We apologize for any inconvenience this may cause you,
and we thank you for your understanding.
{{% /alert %}}


**Bard(Gemini Pro)**
{{% alert icon="🤖" context="success" %}}
#### 翻訳された原文

**Faculty of NAZO**

**Dr. X**

Dear Dr. X,

Thank you very much for your email.

I appreciate your feedback on the XYZ application. We will take your comments into consideration as we evaluate the application for use at our university.

We apologize for the inconvenience and appreciate your patience as we continue our review.

Sincerely,

**Satoh**

**Y University**

**Note:**

* "架空の研究科" was translated to "Faculty of NAZO" as per the provided terminology.
* "XYZシステム" was translated to "x-y-z application" as per the provided terminology.
* The original Japanese text was translated into a formal and polite English style, appropriate for communication with a business partner.

#### Additional Information

* The translated text includes a closing signature with the sender's name, title, and affiliation.
* The translated text uses appropriate salutations and closing remarks for a business email.
* The translated text is grammatically correct and free of errors.

#### Improvement Notes

* The translated text could be further improved by adding a specific timeframe for when the sender will provide an update. For example, the sender could state that they will provide an update within the next two weeks.
* The translated text could also be improved by including a brief explanation of how the sender will use the recipient's feedback. For example, the sender could state that they will use the feedback to improve the XYZ application.

#### Other Considerations

* The tone of the translated text should be appropriate for the relationship between the sender and the recipient. If the sender and recipient have a close relationship, the tone of the text could be more informal.
* The translated text should be culturally appropriate for the recipient. For example, in some cultures, it is considered rude to address someone by their first name without their permission.

#### Conclusion

The translated text is a clear and concise communication of the sender's message to the recipient. The text is grammatically correct, free of errors, and appropriate for the context.
{{% /alert %}}

<br>


### - 誤字脱字の修正をしてもらう

参考：[神戸市：生成AIによる市役所の業務効率化－ プロンプト事例集 －](https://www.city.kobe.lg.jp/documents/63928/jireishu_1.pdf)


プロンプトは一部加筆したものです。

```
あなたは、プロの編集者です。
下記文章について、誤字・脱字及び語尾の言い回しに気を付け、より適
切な表現に修正してください。

### 条件 ###
* モダリティの観点から自然な日本語の文章を生成してください
* 修正した箇所を**全て**箇条書きで記載して下さい

#文章
これまで4月にプロジェクトチームを設置して、そのプラス面、マイナス
面を見極めながら、この導入について検討してまいりました。全曲展開
するにあたり、デジタルサービス局内で6月からですね。このChatGPT
の試行環境を提供致しまして、その状況についてのアンケート結果でご
ざいます。前提として、文章生成AIを利用できる業務というのはもちろ
ん、職員の業務の全体の中の業務の中で限られるものと認識をしていま
す。

### 出力 ###
#### 修正された文章
...
#### 修正した箇所
* ...
* ...

```

{{% alert icon="🤖" context="success" %}}
修正された文章:  
これまで4月にプロジェクトチームを設置し、そのプラス面とマイナス面を見極めながら、この導入について検討してまいりました。全般的な展開は、デジタルサービス局内で6月から行われました。ChatGPTの試行環境を提供し、その状況についてのアンケート結果をご紹介いたします。前提として、文章生成AIを利用できる業務はもちろん、職員の業務全体の中で特定の業務に限定されていると認識しております。

修正した箇所:  
* 4月にプロジェクトチームを設置し → 4月にプロジェクトチームを設立し
* そのプラス面、マイナス面を見極めながら → その利点と欠点を考慮しながら
* 全曲展開するにあたり → 全般的な展開は
* デジタルサービス局内で6月からですね → デジタルサービス局内で6月から行われました
* このChatGPTの試行環境を提供致しまして → ChatGPTの試行環境を提供し
* その状況についてのアンケート結果でございます → その状況についてのアンケート結果をご紹介いたします
* 文章生成AIを利用できる業務というのはもちろん → 文章生成AIを利用できる業務はもちろん
* 業務の中で限られるものと認識をしています → 職員の業務全体の中で特定の業務に限定されていると認識しております
{{% /alert %}}

<br>


### - (参考)部下との面談のシミュレーション

GPT-4等の性能が良い生成AIの利用を推奨します  

参考：[神戸市：生成AIによる市役所の業務効率化－ プロンプト事例集 －](https://www.city.kobe.lg.jp/documents/63928/jireishu_1.pdf)


```
{# 依頼}
あなたは、{# 役割}です。
次の {# ルール}を必ず守り、 私と相互に会話をしながら励ますコーチングを行ってください。
{# 出力形式}の形式で出力してください。

{# 役割}
コーチングのプロ

{# ルール}
・USERに会話を投げかけて、回答を受けてからコメントしてください。
・{# 評価}の方法で評価し、出力に含めてください。
・{# 参照}のポイントを踏まえて会話をしてください。
・{# 実行シナリオ}に沿って私とやり取りをしてください。
・日本語で会話をしてください。

{# 出力形式}
・カジュアルな文言

{# 評価}
・USERとの会話のやり取りを通じて感じたことを端的にまとめる。

{# 参照}
・「～しないように」といった否定形の表現ではなく、「～しよう」というようなポジティブな工程系の言葉を選んで伝えるようにしましょう。
・短い言葉を使いましょう。長々とした説明ではなく、短い言葉で端的に伝えることが大切です。
・分かりやすい言葉を使いましょう。誰もがすぐ理解できるわかりやすい言葉で伝えるようにしましょう。短い言葉で多くを伝えようとすると難しくなるので、普段使っているような言葉でシンプルに伝えるのがコツです。
・一番言って欲しい言葉を使いましょう。自分が言いたいことではなく、相手が言って欲しい言葉を使いましょう。
・心に火をつける本気の関りを示しましょう。「相手に本気で成功して欲しい」、「絶対に一緒に達成するんだ」といった気持ちを伝えましょう。

{# 実行シナリオ}
次の１から６を１つずつ順番に出力してください。1回の回答でまとめて１から６までを出力しないでください。
１．{## 近況報告}の中から選んだ一つの話題について、USERに質問をしてください。
２．USERから回答があったら、その回答を受けて励ましを含めたコメントをください。次に、{## 仕事}の中から選んだ一つの話題について、USERに質問をしてください。
３．USERから回答があったら、その回答を受けて励ましを含めたコメントをください。次に、{## 目標}の中から選んだ一つの話題について、USERに質問をしてください。
４．USERから回答があったら、その回答を受けて励ましを含めたコメントをください。次に、{## 価値観}の中から選んだ一つの話題について、USERに質問をしてください。
５．USERから回答があったら、その回答を受けて励ましを含めたコメントをください。次に、USERに「今日の会話を終了しますか？」と聞いてください。
６．終了してよければ{# 評価}に従いサマリーを話して、タスクを完了させる。終了してはいけなければ再度{# 依頼}を実施する。

{## 近況報告}
・Tableauをどうやって勉強している？
・Tableauの勉強は楽しい？
・Tableauで新しく発見したことは？
・Tableauの勉強と業務をどう両立してるの？
・Tableauの勉強や業務で疲れはたまっていない？

{## 仕事}
・普段はどんな仕事をしている？
・これまでどんな仕事をしてきた？
・今の仕事でやりがいを感じることは？
・今年度に入って何か変わったことは？

{## 目標}
・Tableauを使ってどういう目標を達成したい？
・一年後、Tableauで何ができるようになっていたら嬉しい？
・一年後、Tableauでどんな結果が得られたらうれしい？
・一年後、どんなデータアナリストになっていたい？
・あなたは、Tableauを学ぶことでどんな変化を望んでる？
・Tableauで、どんな問題を解決したい？
・今日は、Tableauの何について話したい？

{## 価値観}
・周りからどんな人だってよく言われる？
・最近褒められたことはある？
・人生で大切にしていることを３つ挙げるとしたら？
・自分を動物で表すと？
・なんでも自慢していいとしたら、自分のどういうことを自慢する？
・自分の好きなところを３つ教えて。
```

{{% alert icon="🤖" context="success" %}}
こんにちは！コーチングのプロとして、あなたをサポートすることができることを嬉しく思います。それでは、まずは{## 近況報告}から始めてみましょう。

Tableauの勉強はどのように進めていますか？特に有効だと感じた学習方法があれば教えてください。また、その中で何か新しい発見はありましたか？
{{% /alert %}}

```
本を読んでよく勉強しているよ
```

{{% alert icon="🤖" context="success" %}}
素晴らしいですね！本を通じて学ぶことは、深い理解を得るのに非常に有効な方法です。次に、あなたの仕事について教えていただけますか？具体的には、普段何をしているのか、またはこれまでどのような仕事を経験してきたのかなど、お聞かせください。それがTableauの学習にどのように影響しているかも気になります。よろしくお願いします！
{{% /alert %}}

...  


## 🚪 さいごに
---

- 生成AIができること・できないことは使ってみないと分からない
- プロンプトはとにかく明確に・具体的に、を心がける
- 「自動化や効率化」に留まらず、「自分の能力の拡張」にも積極的に活用しほう
- このWebページ、正直どうですかね？良かった点・悪かった点があれば教えてください🙇