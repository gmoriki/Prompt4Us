---
weight: 5
title: "大学職員・URAのためのCopilotセミナー"
description: "2024年度「大学職員・URAのためのCopilotセミナー」の講演資料アーカイブ"
icon: "article"
date: "2024-02-03T20:55:25+09:00"
lastmod: "2024-02-03T20:55:25+09:00"
draft: false
toc: true
aliases:
  - /docs/archive/hands-on-for-RA2024/
---

{{% alert context="warning" %}}
この資料は2024年12月の講演時点の内容です。最新のプロンプト例は[プロンプト集]({{% relref "/docs/cases/" %}})をご参照ください。
{{% /alert %}}

{{< table "table-responsive" >}}
| 日時 | このページで使用した生成AI |
|----------|--------------|
| 2024/12/18 | Copilot |
{{< /table >}}

#### 使用する主な生成AI：
{{< table "table-striped" >}}
| 名称                                              | 説明                                                      |
|---------------------------------------------------|-----------------------------------------------------------|
| [Copilot](https://copilot.microsoft.com/)         | Microsoft社が開発・提供する対話型生成AIサービス          |
{{< /table >}}


#### その他生成AI：
{{< table "table-striped" >}}
| 名称                                              | 説明                                                      |
|---------------------------------------------------|-----------------------------------------------------------|
| [ChatGPT](https://chatgpt.com/)               | OpenAI社が開発・提供する対話型生成AIサービス              |
| [Gemini](https://gemini.google.com/chat)              | Google社が開発・提供する対話型生成AIサービス              |
| [Claude](https://claude.ai/)                      | Anthropic社が開発・提供する対話型生成AIサービス           |
| [Perplexity](https://www.perplexity.ai/)          | Perplexity AI社が開発・提供する対話型生成AIサービス      |
{{< /table >}}


## 文章を要約する


参考：[文章自動要約の例文](https://www.hitachi-solutions-east.co.jp/products/coreexplorer_ts/example/)

```markdown
以下の文章を要約してください。

Excel でプロジェクトの日程管理をしている企業は多い
Excel はオフィス業務に欠かせないアプリケーションであり、多くの人が慣れ親しんでいるスタンダードツールだ
しかし、複数プロジェクトが関連しあって同時進行していると、変更の際の整合性が課題となる
大手情報関連機器メーカーでは、大日程管理の対象機器が年間数百種に及び、さらにその中日程、小日程があり、膨大な数になっていた
これらが同時に進み、その調整や変更への対応が従来の管理方法では限界を超えていた
グループ全体でのプロジェクト管理の標準化や効率化、さらには同社の推進するIT 戦略の一環として、対策を検討
そこで、採用されたのが日立ソリューションズ東日本の提供する工程管理・プロジェクト管理ツール『SynViz S2』であった
採用の決め手となったのがシャドウ機能だ
関連する日程表を別の日程表に貼り付けると、元の日程表の変更がリアルタイムに反映される
例えば、中日程に貼り付けられた大日程の予定が変更されても、見逃すことがなくなる
同社ではアドオンで大日程・中日程・小日程間を連携する機能も追加した
Excel の使いやすさと見やすさそのままに、SynViz S2 に備わった機能の利便性が高く評価され、全社での展開が進められている
さらに海外生産拠点での導入も視野に入ってきた
```

```markdown
# 命令書:
あなたは{プロの編集者}です。
以下の制約条件と入力文をもとに{最高の要約}を出力してください。

# 制約条件:
- 簡潔に本質が理解できるようなストーリー(背景、課題、ソリューション)を採用する
- 重要なキーワード「効率化」を強調する
- 最後に####備考 を設け、表計算ソフト・Excelについて一言で解説する
- 回答は300文字

# 入力文：
Excel でプロジェクトの日程管理をしている企業は多い
Excel はオフィス業務に欠かせないアプリケーションであり、多くの人が慣れ親しんでいるスタンダードツールだ
しかし、複数プロジェクトが関連しあって同時進行していると、変更の際の整合性が課題となる
大手情報関連機器メーカーでは、大日程管理の対象機器が年間数百種に及び、さらにその中日程、小日程があり、膨大な数になっていた
これらが同時に進み、その調整や変更への対応が従来の管理方法では限界を超えていた
グループ全体でのプロジェクト管理の標準化や効率化、さらには同社の推進するIT 戦略の一環として、対策を検討
そこで、採用されたのが日立ソリューションズ東日本の提供する工程管理・プロジェクト管理ツール『SynViz S2』であった
採用の決め手となったのがシャドウ機能だ
関連する日程表を別の日程表に貼り付けると、元の日程表の変更がリアルタイムに反映される
例えば、中日程に貼り付けられた大日程の予定が変更されても、見逃すことがなくなる
同社ではアドオンで大日程・中日程・小日程間を連携する機能も追加した
Excel の使いやすさと見やすさそのままに、SynViz S2 に備わった機能の利便性が高く評価され、全社での展開が進められている
さらに海外生産拠点での導入も視野に入ってきた

# 出力文：
3点(背景、課題、ソリューション)に箇条書き
#### 備考
...
```


## 相談する

```markdown
無条件に褒めてくれ〜〜でも無理に頑張れと言って私を鼓舞させるのではなく、ありのままの私を認めてほしい。あなたの回答の一言一句が私の労働生産性に直結します。
```

```markdown
月曜日らやる気が出ないです、どうすればいいですか
```

```markdown
大学業界におけるURAの重要性と、URAの成果創出に時間がかかる背景と理由を、大学の他部署の人にでもわかるように説得して
```

## Web検索する

```markdown
国内大学のオープンアクセス加速化事業の現状は？
```

```markdown
香港理工大学の生成AIポリシーは？
```

```markdown
このリンクを参照してくださいhttps://libguides.lb.polyu.edu.hk/online-tools-for-assignment/GenAI_tools
```

```markdown
香港理工大学の生成AIガイドラインについて教えてください。表形式でわかりやすく整理すること。https://libguides.lb.polyu.edu.hk/online-tools-for-assignment/GenAI_tools
```

## 研究広報の文章を作成する

参考：[論文情報](https://onlinelibrary.wiley.com/doi/abs/10.1002/ir.20329)

```markdown
## ステップ1：自然な日本語への翻訳
学術論文を、専門用語の正確性を保ちながら自然な日本語に翻訳してください。

## ステップ2：読者層別の表現変換
ステップ1で作成した日本語訳を、以下の3つの読者層向けに変換してください。

### 学内教職員向け
- 具体的な実務への応用点
- 現状の課題と改善案
- 実装における留意点
- 組織内での位置づけ
- 類似事例との比較

### 政策立案者・評価機関向け
- 政策との整合性
- 制度的な意義
- 組織的な体制整備の観点
- 客観的指標や効果
- 国際的な文脈

### 広報・メディア向け
- 社会的意義
- 具体的な成果や効果
- 受益者へのメリット
- わかりやすい事例
- 独自性や新規性

## 注意事項
- まずは専門的な正確性を保持した日本語訳を作成
- 各読者層の視点や理解度に応じた表現に変換
- 研究の本質的な意義が失われないよう留意

### 原文
Data Governance 101: IR's Critical Role in Data Governance
Building a culture of data governance at a higher education institution involves collaboration across the entire institution. Before the creation of formalized roles to perform data management and data governance functions at colleges and universities, these functions were performed by traditional institutional research personnel. Documentation and management of data for analysis have, for a long time, been part of the institutional researcher's forte. However, a concentrated effort in data management and governance is necessary to transform traditional reporting into a dynamic analytic landscape complete with adequate definitions and documentation, and often this goes beyond the scope of today's institutional research offices. The following article offers a framework for developing a data governance program in a higher education setting and highlights the critical role that institutional research offices can play in helping to build institutional capacity for a well-documented and managed data landscape. Support and rationale for developing a program at your institution are offered, and helpful tips and pitfalls to avoid are provided.
```


## 参考文献一覧の変換

参考：[大学行政管理学会誌執筆要領](https://juam.jp/new6358/)

```markdown
あなたは参考文献製造マシーンです。私が文献情報を入れると、下記ルールに従って参考文献を書き直してください。
出力は端的に回答を返してください。わかりましたか？

### ルール
文献の記載については、著者名（発行年）：論文タイトル（著書名）、学術雑誌名（出 版社名）、ページ番号等の順序形式とし、具体的には以下のようにする。 イ 雑誌論文の場合 著者名（発行年）：論文タイトル、学術雑誌名、巻（号）、ページ番号 （例）鈴木一郎（2015）：アドミニストレーター養成に関する分析、大学行政管理 学会誌、18（3）、pp.1-10 Suzuki I（2015）: Analysis of Training for Administrator, Japan Journal of University Administrative Management, 18（3）, pp.1-10 ロ 書籍の場合 著者名（発行年）：『書籍名』、出版社名 （例）鈴木一郎（2015）：『アドミニストレーター養成』、大学行政管理学会 Suzuki I （ 2015 ）： Training for Administrator, Japan Association of5 University Administrative Management ハ 編著・分担執筆の一部の場合 著者名（発行年）：分担執筆した部分のタイトル、編著者名『書籍名』、出版社名、 分担執筆したページ番号 （例）佐藤花子（2015）：アドミニストレーターの必要性、鈴木一郎編『アドミニ ストレーター養成』、大学行政管理学会、pp.5-10 Sato H（2015）: the Necessity of Administrator, Suzuki I ed. Training for Administrator, JUAM, pp.5-10 ニ ホームページの場合 （例）大学行政管理学会（2015）：学会誌への投稿について、http://juam.jp/wp/im/ publish/submit/、閲覧日 2015 年 12 月 25 日 ホ 文献は、日本語文献（著者 50 音順）、英語文献（著者アルファベット順）の順と し、同一著者によるものはそれぞれ発行年の順に並べて、同じ発表年のものが複数あ る場合には、引用順にａ、ｂ、ｃ･･･として並べること。

#### 入力例

*森木 銀河, 大学職員のためのプロンプトガイドの開発, 大学情報・機関調査研究集会 論文集, 2024, 13 巻, 第13回大学情報・機関調査研究集会　論文集, p. 175-181, 公開日 2024/11/20, Online ISSN 2436-3014, Print ISSN 2436-3065, https://doi.org/10.50956/mjir.13.0_175_1, https://www.jstage.jst.go.jp/article/mjir/13/0/13_175_1/_article/-char/ja, 

#### 出力例
森木銀河（2024）：大学職員のためのプロンプトガイドの開発、大学情報・機関調査研究集会論文集、13、pp.175-181
```

{{% alert icon="" context="warning" %}}
**注意**: 上記プロンプト内のルール例に含まれるURL（`http://juam.jp/wp/im/`）は現在アクセスできません。最新の執筆要領は[大学行政管理学会のサイト](https://juam.jp/new6358/)をご確認ください。
{{% /alert %}}


## 企画書の作成(広報活動)

```markdown
大学でAIイベントを実施するので企画書を書いて
```

```markdown
あなたは大学広報イベントの企画のスペシャリストです。
以下の要件に従って、魅力的な広報イベントの企画案を作成してください。

### 入力情報 ###
[以下の情報を可能な範囲で記入してください]

イベントの目的：
対象者：
希望時期：
予算目安：
会場：
特にアピールしたい学部/研究：

### 要件 ###
* 大学の特色や強みを効果的に伝える内容を含める
* 参加者が能動的に参加できる要素を組み込む
* SNSでの拡散を意識した企画を含める
* 実現可能性の高い提案を心がける
* 学生・教職員の負担に配慮する
* 費用対効果を意識する

### 出力形式 ###
以下の構造で企画案を提供してください：

1. イベントコンセプト（50字以内）
2. 企画概要（300字程度）
3. プログラム案
4. 必要な準備・リソース
5. 期待される効果

### 補足 ###
* 天候対策が必要な場合は代替案を記載
* 特殊な機材や許可が必要な場合はその旨を明記
* 過去の成功事例や他大学の事例も参考に提案
```

追加の指示案：

```markdown
企画書を表形式に整理してください
```

```markdown
他のイベントコンセプト案を5つ挙げてください。そのコンセプト名の理由も教えてください。
```


## 参考文献

{{< table "table-striped" >}}
| 書籍名                                                                                      | 著者名      | 出版年月日   | 備考                                                         |
|-------------------------------------------------------------------------------------------|-----------|------------|------------------------------------------------------------|
| [AI時代の質問力 プロンプトリテラシー 「問い」と「指示」が生成AIの可能性を最大限に引き出す](https://www.shoeisha.co.jp/book/detail/9784798188102)             | 岡 瑞起,橋本 康弘 | 2024/07/10 | 利用者に必要とされるプロンプトリテラシーおよび今後のAIエージェントの展望を示した**必読書**   |
| [都職員のアイデアが詰まった文章生成AI活用事例集](https://www.digitalservice.metro.tokyo.lg.jp/documents/d/digitalservice/ai_prompt/) | 東京都が公開している事例集 |
| [デジタル庁検証資料](https://www.digital.go.jp/news/19c125e9-35c5-48ba-a63f-f817bce95715)| 2023年度 デジタル庁・行政における生成AIの適切な利活用に向けた技術検証 |
{{< /table >}}

<script>
 window.difyChatbotConfig = {
  token: '6jfuLWqu0wJCZdjH'
 }
</script>
<script
 src="https://udify.app/embed.min.js"
 id="6jfuLWqu0wJCZdjH"
 defer>
</script>
<style>
  #dify-chatbot-bubble-button {
    background-color: #0BA272 !important;
    width: 64px !important;  /* アイコンの幅を増やす */
    height: 64px !important; /* アイコンの高さを増やす */
  }
  #dify-chatbot-bubble-button svg {
    width: 32px !important;  /* SVGアイコン自体のサイズも大きくする */
    height: 32px !important;
  }
</style>