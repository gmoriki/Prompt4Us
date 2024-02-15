  ---
weight: 999
title: "[作成中]ChatGPTハンズオンの会"
description: "主催：教職員能力開発拠点（愛媛大学教育・学生支援機構教育企画室）"
icon: "article"
date: "2024-02-09T15:13:55+09:00"
lastmod: "2024-02-09T15:13:55+09:00"
draft: true
toc: true
---

2024年2月17日に開催する[大学職員のためのChatGPTハンズオンの会](https://web.opar.ehime-u.ac.jp/info/chat-gpt/)用ページです。

{{< table "table-responsive" >}}
| 日時 | このページで使用した生成AI | 
|----------|--------------|
| 2024/02/03 | ChatGPT(GPT-3.5) <br> 一部でBardやCopilotを紹介 |
{{< /table >}}
<br>

## 🎯 目標
---

{{% alert icon="" context="light" %}}
1. **全員が「ChatGPTを利用したことがある人」になる**
2. **行動の選択肢に「生成AIを使う」が入る**
3. **全員が「長い文章を好きなように要約できる人」になる**
{{% /alert %}}

以下の「要約したい文章」を「生成AIによって要約された文章」へ変換できるようになりましょう。  
※ **プロンプトとは生成AIに対する指示文・命令文のことです。**

##### 要約したい文章

{{% alert icon="📖" context="light" %}}
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
参考：[文章自動要約の例文](https://www.hitachi-solutions-east.co.jp/products/coreexplorer_ts/example/)
{{% /alert %}}


##### 生成AIによって要約された文章

{{% alert icon="🤖" context="success" %}}
- 多くの企業がExcelを使用し、プロジェクトの日程管理に役立てている。
- しかし、複数プロジェクトの同時進行により変更の整合性が課題となっている。
- 日立ソリューションズ東日本の『SynViz S2』は、Excelの使いやすさを保ちながら、プロジェクト管理の効率化を実現する新たな解決策として採用された。

#### 備考
Excelはオフィス業務で幅広く使用される表計算ソフトであり、プロジェクト管理などのさまざまなタスクに利用される。
{{% /alert %}}

<br>


ハンズオンの会ははじめてChatGPTを利用する方に向けた内容ですが、もし余裕がある人は  
**プロンプトをどのように書けばこの要約が可能か？** を考えてみてください。

<br>


## 📝 主にChatGPT(無料版)を使います
---

2024年2月現在、**対話型生成AIサービス**は大量に公開されています。  

{{% alert icon="📖" context="light" %}}
例えば[TAAFT](https://theresanaiforthat.com/)では**11,960**個ものAIツールが紹介されています(2024年2月16日時点)。  
日本語で検索したい場合は[sayhi2.ai](https://sayhi2.ai/ja/product?ordering=-popularity_score)をご参照ください。5000以上のAIツールを紹介しているそうです。
{{% /alert %}}

その中でも**メジャーな対話型文章生成AIサービス**を4つ、ざっくり紹介します。

* [ChatGPT](https://chat.openai.com/ "ChatGPT")
  * OpenAIが開発・提供する生成AI
  * 王道
* [Copilot](https://copilot.microsoft.com/ "Copilot")
  * Microsoftが開発・提供する生成AI
  * OpenAIが開発したAIモデルを活用した検索エンジン
  * 元Bing AI
* [Gemini](https://gemini.google.com/chat "gemini")
  * Googleが開発・提供する生成AI
  * Google関連アプリケーションとの連携が可能
  * 元Bard
* [Claude](https://claude.ai/ "Claude")
  * Anthropicが開発・提供する生成AI
  * Amazonによる多額の出資を受けている
  * 元OpenAIの人たちが立ち上げた

それぞれ無料版/有料版がありますが、。  
今回は **ChatGPT(無料版)** を利用する想定で説明します。  
その上で、要所要所でCopilotやGeminiを利用するかもしれません。  

Copilotはアカウント不要ですが、他はGoogleアカウント等が必要です。

{{% alert icon="❓" context="info" %}}
##### なぜChatGPT(無料版)を利用するのか
そこまで深い理由ではありません。

1. **GPTを使ったサービスが極めて多いから**
     - ChatGPTの中で使用されているLLMであるGPTは、既にCopilotや法人GAIなどへ広く取り入れられている
     - AIと言えばChatGPTみたいな風潮があり、AIの性能やリスクもChatGPTありきで議論される雰囲気がある
2. **大規模言語モデル(LLM)の特長を理解できるから**
     - 特に無料版を利用する場合、回答の精度や質はCopilotやGeminiの方が優れていることが多い。しかしこれらはLLMを活用した検索エンジンなので、LLMそのものの特長とは結び付かない部分が多い
     - ChatGPT(無料版)は素朴であるがゆえに、今後、他の生成AIサービスを利用時に応用が効く
3. **シンプルだから**
      - いいよね...

{{% /alert %}}

もちろん**他の生成AIサービスを利用しても問題ありません。**


<br>



## 🚩 はじめてのChatGPT
---

### - まずはあいさつする

```
おはようございます。今日の天気は雨です。
```

{{% alert icon="🤖" context="success" %}}
おはようございます。雨の日ですね。傘を持って外出されることをお勧めします。何かお手伝いできることがありましたら、お知らせください。
{{% /alert %}}

### - 質問してみる

```
大学事務職員が使う台車の種類を3つ教えてください
```

{{% alert icon="🤖" context="success" %}}
大学事務職員が使う台車の種類は、以下のようなものがあります。

1. 書類や文具を運搬するための折りたたみ式の手押し台車：大学内で書類や文具を移動させる際に便利な台車です。折りたたみ可能なため、収納や移動時に場所を取りません。

2. イベントやセミナーで使用する展示物や資料を運搬するための展示用台車：大学のイベントやセミナーで使用される展示物や資料を運ぶための専用の台車です。展示物の安全な移動や設置に役立ちます。

3. 教室やオフィスでの清掃作業に使用する清掃用台車：教室やオフィスの清掃作業に必要な備品や清掃用具を運搬するための台車です。掃除機やモップ、掃除剤などをまとめて運ぶことができます。
{{% /alert %}}

### - 変なスタイルで回答させる

```
大学事務職員が使う台車の種類を3つ教えてください
愉快な関西弁で
```
※ Shift＋Enterで改行できます

{{% alert icon="🤖" context="success" %}}
おおっ、せやなぁ〜！大学の事務職員が使う台車やったら、まず最初は「書類運び台車」やで！あれは書類や文房具を運ぶのにピッタリやねん。ちょっとした移動も楽勝やで！

次にあるのは「イベント準備用の台車」やないかな。大学でのイベントやセミナーの準備には欠かせへんやろ？あれを使って、椅子やテーブル、備品を運ぶんやで！

最後に大事なのは「アーカイブ用の台車」やねん。古い文書や資料を整理する時に、あれはめっちゃ役立つで。大学の歴史や記録を整理する時には欠かせへんやろう！
{{% /alert %}}

### - 今日はよろしくね

```
ありがとう！こうやって今日はあなたとお話しします。よろしくお願いします。
```

{{% alert icon="🤖" context="success" %}}
ええ、おおきに！わしとのおしゃべり、楽しんでくれてうれしいわ。今日もなにかあったら、なんでも聞いてくれや。よろしく頼むで！
{{% /alert %}}

<br>


## 🏳‍🌈 生成AIをなぜ使うのか？
---

今日は「大学職員のためのChatGPTハンズオンの会」ですので、大学の業務に活用したい方が多いのではないでしょうか。その点を掘り下げて、実際のプロンプトを使いながら考えてみましょう。


#### - 業務を効率化・自動化するため

耳にタコができるほど聞きましたね。  

既存の業務を効率的・自動的に処理したい、というモチベーションが目的になる場合が多いです。

{{% alert icon="📖" context="light" %}}

例えば東京都が公開した[都職員のアイデアが詰まった文章生成AI活用事例集](https://www.digitalservice.metro.tokyo.lg.jp/documents/d/digitalservice/ai_prompt/)ではこの点が強調されており、実際に「業務効率化・質の向上などに一定の効果があること」が明らかになっています。

東北大学の藤本さんが先日発表した[東北⼤学が推進する"⽣成AIの業務実装"](https://www.nii.ac.jp/event/upload/20240207-3_fujimoto.pdf)では法人GAI(組織内に導入された対話型文章生成AIサービス)を導入し、主に「通知文等の日本語、英語の構成」(21.6%)、「あいさつ文、通知文等の作成」(19.6%)、「コーディング」(17.6%)に使用していることが示されています。
{{% /alert %}}


東京都の事例より**誤字脱字の修正をしてもらう**を引用します。

```
あなたは、プロの編集者です。
下記文章について、誤字・脱字及び語尾の言い回しに気を付け、より適切な表現に修正してください。

#文章
これまで4月にプロジェクトチームを設置して、そのプラス面、マイナス面を見極めながら、この導入について検討してまいりました。全曲展開するにあたり、デジタルサービス局内で6月からですね。このChatGPTの試行環境を提供致しまして、その状況についてのアンケート結果でございます。前提として、文章生成AIを利用できる業務というのはもちろん、職員の業務の全体の中の業務の中で限られるものと認識をしています。
```

{{% alert icon="🤖" context="success" %}}
これまで、4月にプロジェクトチームを設立し、そのプラス面とマイナス面を見極めながら、この導入について検討してまいりました。全体の展開にあたり、デジタルサービス局内では6月からとなります。ChatGPTの試行環境を提供し、その状況についてのアンケート結果を取得しました。文書生成AIの利用は、職員の業務全般ではなく、特定の業務に限定されると認識しています。
{{% /alert %}}



##### 勉強するため

こちらは拡張です。

```
プログラミング言語Pythonって何？Excelと何が違う？事務業務で使うメリットは？
私は初心者なので、厳密さよりも分かりやすさを優先して説明してください。
言葉もかんたんにして
```
{{% alert icon="🤖" context="success" %}}
Pythonは、プログラミング言語の一種で、コンピューターに指示を出すための特別なルールや文法の集まりです。Excelと違うのは、Excelは表計算ソフトウェアであり、主に数字やデータを整理し、計算したりグラフにしたりするのに使います。Pythonは、Excelよりも柔軟性があり、さまざまなタスクを自動化したり、大量のデータを処理したり、Webサイトを作ったりすることができます。

事務業務でPythonを使うメリットはいくつかあります。例えば、繰り返しの作業を自動化したり、大量のデータを効率的に処理したりできます。また、Pythonは比較的簡単な言語であり、初心者でも学びやすいので、新しいスキルを身につけるのが容易です。
{{% /alert %}}

```
次の3つのステップで、私の仮説を改善してください。

### 仮説 ###
大学事務職員は技術の進展に疎いのでダメ

### ステップ ###
- 仮説の特長を批判的かつ建設的に分析する
- 明るい未来をつくるための提言に言い換える
```

##### 両者は相補う関係


## ⚠️ 生成AIを利用することのリスク
---
簡単な挨拶も済んだのでChatGPTをどんどん使っていきたいところですが、  
その前に知っておきたい生成AIの性質(**限界**)やリスク(**課題**)についてご説明します。


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


## 🌷 適切な生成AI利用
---

ああ

<div class="row flex-xl-wrap pb-4">

<div id="list-item" class="col-md-4 col-12 py-2">
  <a class="text-decoration-none text-reset" href="../../essence/mindset">
  <div class="card h-100 features feature-full-bg rounded p-4 position-relative overflow-hidden border-1">
      <span class="h1 icon-color">
        <i class="material-icons align-middle">Reminder</i>
      </span>
      <div class="card-body p-0 content">
        <p class="fs-5 fw-semibold card-title mb-1">生成AIの扱い方</p>
        <p class="para card-text mb-0">生成AIと付き合う姿勢を理解する</p>
      </div>
    </div>
  </a>
</div>

</div>

あまりよくない例： ※ 検索エンジンを兼ねた生成AIであればリスクをおさえられます。
```
鎌倉幕府　いつから
```
{{% alert icon="🤖" context="success" %}}
鎌倉幕府は、日本の歴史において、1185年から1333年まで存在した武士政権です。鎌倉幕府の成立は、1185年に源頼朝が壇ノ浦の戦いで平氏を打倒し、鎌倉に幕府を開くことに始まります。この時期は鎌倉時代とも呼ばれ、鎌倉幕府は武士の政権として、日本の支配を行いました。鎌倉幕府は、鎌倉時代の終焉である1333年の建武の新政によって滅ぼされ、南北朝時代へと移行しました。
{{% /alert %}}


より良い使い方の一例：
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


## 🚩 ChatGPTを活用してみよう
---

生成AIの限界と課題、使い方の基本を理解できたら、日々のお仕事や日常の中で活用したいですよね。  
大学職員による報告や事例集はほとんど報告されていないので、ここでは自治体が公開している事例集を主に紹介します。

### - 話し言葉からビジネスメールを作成する

参考：[東京都：都職員のアイデアが詰まった文章生成AI活用事例集](https://www.digitalservice.metro.tokyo.lg.jp/documents/d/digitalservice/ai_prompt/)

```
以下の内容を基に、日本語のビジネスメールのベストプラクティスに従い、わかりやすく、整理された清書を作成してください。

東京太郎様。先日審査会ありがとう。御社の提案は不採用。すみません。新宿花子より
```

{{% alert icon="🤖" context="success" %}}
件名: 審査結果についてのご連絡

東京太郎様

先日は、審査会にご参加いただきありがとうございました。この度は、貴社からの提案に対して審査を行いましたが、残念ながら不採用とさせていただきますことをお知らせいたします。

何卒ご理解いただけますようお願い申し上げます。また、今後ともご支援を賜りますようお願い申し上げます。

尚、ご不明点や疑問点がございましたら、お気軽にご連絡ください。

敬具

新宿花子
{{% /alert %}}


### - Excelの関数を作ってもらう

参考：[東京都：都職員のアイデアが詰まった文章生成AI活用事例集](https://www.digitalservice.metro.tokyo.lg.jp/documents/d/digitalservice/ai_prompt/)

```
# 指示
局内講習会の参加者リストにおける「参加可否」列に“参加”もしくは“不参加”を入力する計算式を作成してください。

# 目的
正確な計算式をエクセルに入力し、参加者の参加可否状況を把握するため

# 情報
・参加可否の条件：
・条件：3つの参加条件（例：参加登録、参加許可、必要な情報の提出）が全て満たされている
・シート構造：A列には参加者名、B列には参加登録状況（1で登録済み、0で未登録）、C列には参加の許可状況（1で許可済み、0は未許可）、D列には必要
な情報の提出状況（1で提出済み、0で未提出）が記載されています。E列に関数を入れたいです。

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

ところで最初の「# 情報」で利用者が想定しているExcelはどのような形でしょうか。  
気になったので訊いてみました。

```
この# 情報で想定されているテーブルデータの例を出力してください
```

{{% alert icon="🤖" context="success" %}}
理解の助けになるよう、指示された情報に基づいて、参加者リストのテーブルデータの例を作成します。以下は想定されるテーブルデータの例です：

```
| 参加者名 | 参加登録状況 | 参加の許可状況 | 必要な情報の提出状況 |
|---------|--------------|----------------|----------------------|
| 参加者A |      1       |       1        |          1           |
| 参加者B |      0       |       1        |          1           |
| 参加者C |      1       |       0        |          1           |
| 参加者D |      1       |       1        |          0           |
| 参加者E |      0       |       0        |          0           |
```

この例では、参加者Aは全ての条件を満たしており、「参加」と判断されるでしょう。参加者Bは参加登録状況が未登録なので「不参加」、参加者Cは参加の許可状況が未許可なので「不参加」、参加者Dは必要な情報の提出状況が未提出なので「不参加」となります。参加者Eは全ての条件を満たしていないので、「不参加」となります。

{{% /alert %}}


このように、出力を表形式に指定することも可能です。


### - １年間の目標を設定して報告する

参考：[東京都：都職員のアイデアが詰まった文章生成AI活用事例集](https://www.digitalservice.metro.tokyo.lg.jp/documents/d/digitalservice/ai_prompt/)


```
# ゴール
組織方針を元に、担当業務を分解してそれぞれの業務における具体的な
行動目標を３つ設定してください

# 担当業務
・生成AI利用のルールを作成し、生成AIの共通基盤を都庁職員向けに導
入する
・生成AIの利用促進を図るため、アイデアソンを複数開催する

# 組織方針
・都庁のＤＸ推進に向けた課題に対応していくため、民間企業等の動向
をはじめ必要かつ十分な情報収集・分析に努め、都庁のＱＯＳ及び都民
のＱＯＬ向上に資する企画立案を行うとともに、効果的な事業化につな
げる。
```

{{% alert icon="🤖" context="success" %}}

担当業務を組織方針に基づいて分解し、それぞれの業務における具体的な行動目標を設定します。

#### 生成AI利用のルールを作成し、生成AIの共通基盤を都庁職員向けに導入する

1. **ルール策定**
   - 都庁のDX推進方針に則り、生成AIの利用に関するルールを作成する。
   - ルールは適切な倫理規定と法的規制を含み、利用範囲やデータの取り扱い方法などを明確にする。

2. **共通基盤構築**
   - 都庁職員が利用しやすい共通基盤を構築する。
   - ユーザーフレンドリーなインターフェースやトレーニングプログラムの提供など、利用促進を図る。

3. **導入プロセスの設計と実行**
   - 生成AIの共通基盤導入のためのプロセスを設計し、実行する。
   - 各部門や職種のニーズを考慮した導入計画を策定し、効果的な導入を支援する。

#### 生成AIの利用促進を図るため、アイデアソンを複数開催する

1. **アイデアソンの企画と実施**
   - 都庁のDX推進方針に基づき、生成AIの活用アイデアを促進するためのアイデアソンを企画する。
   - 開催時期や参加者の選定、テーマ設定などを適切に決定し、実施する。

2. **参加者の動機付け**
   - 都庁職員や関連ステークホルダーに対し、アイデアソンへの積極的な参加を促す。
   - 利益や成果共有、アイデア採用の機会提供など、参加の動機付けを行う。

3. **アイデアの実装支援**
   - アイデアソンで生まれた優れたアイデアを実際の業務に落とし込む支援を行う。
   - 実装可能性の調査や必要なリソースの提供、プロジェクトチームの形成などをサポートする。

これらの行動目標によって、組織方針に沿った生成AIの活用促進と効果的な導入が実現されるでしょう。
{{% /alert %}}



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

## 🚩 ChatGPTをもっと活用してみよう
---

### - 文章を要約する

```
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

{{% alert icon="🤖" context="success" %}}
- 多くの企業がExcelを使用し、プロジェクトの日程管理に役立てている。
- しかし、複数プロジェクトの同時進行により変更の整合性が課題となっている。
- 日立ソリューションズ東日本の『SynViz S2』は、Excelの使いやすさを保ちながら、プロジェクト管理の効率化を実現する新たな解決策として採用された。

#### 備考
Excelはオフィス業務で幅広く使用される表計算ソフトであり、プロジェクト管理などのさまざまなタスクに利用される。
{{% /alert %}}

### - プロダクト名を考えてもらう
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

### - 会議の時間配分と次第を作成する

参考：[東京都：都職員のアイデアが詰まった文章生成AI活用事例集](https://www.digitalservice.metro.tokyo.lg.jp/documents/d/digitalservice/ai_prompt/)


```
以下の条件の基に会議を開催したいので、議事次第を作成してください。

＃会議参加者
東京都職員

＃条件
・議論の進行順に番号をつけて箇条書きにしてください。
・会議時間は1時間。
・時間配分も記載する。

＃会議内容
・文章生成AI(ChatGPT)の利用者数の効果的な利用
・利用者増の施策を検討。
```

{{% alert icon="🤖" context="success" %}}
**会議議事次第**

**日付:** [会議日付を記入]

**時間:** [開始時刻 - 終了時刻]

**場所:** [会議場所を記入]

**出席者:**
- [参加者1]
- [参加者2]
- [参加者3]
- [参加者4]
- [参加者5]

---

**議題: 文章生成AI(ChatGPT)の効果的な利用と利用者増の施策検討**

**議事進行:**
1. **開会と挨拶** (5分)
   - 開会宣言と出席者への挨拶。
   
2. **議題説明** (10分)
   - 文章生成AI(ChatGPT)の現状と今後の利用方針について説明。
   - 利用者数の増加に向けた施策の必要性について説明。

3. **現状の分析と議論** (15分)
   1. ChatGPTを利用している部署やプロジェクトについての現状把握。
   2. ChatGPTの利用に関する課題や問題点の洗い出し。
   3. 他の部署や企業が成功しているChatGPTの利用事例の共有。

4. **施策の検討** (20分)
   1. ChatGPTの利用促進策についてのアイデア出し。
   2. 具体的な利用者増加施策の提案と議論。
   3. 利用者のニーズに合ったChatGPTの改善点の提案。

5. **採択する施策の決定** (5分)
   - 議論を元に採用する施策の選定。

6. **次回会議の日程調整と閉会** (5分)
   - 次回の会議日程を決定し、閉会。

**閉会:** [閉会時刻を記入]

---

**備考:**
- 上記の時間配分は目安であり、議論の進行状況に応じて調整することが可能です。
- 議題に関する資料やデータがある場合は、事前に参加者に配布しておくと議論がより効果的に進行するでしょう。
{{% /alert %}}


### -  文章を改善する




<br>

## 🚪 さいごに
---

##### 目標のおさらい

{{% alert icon="" context="light" %}}
✅ **全員が「ChatGPTを利用したことがある人」になる**  
✅ **行動の選択肢に「生成AIを使う」がチラつくようになる**  
✅ **全員が「長い文章を好きなように要約できる人」になる**  
{{% /alert %}}


##### ポイント

- AIをあなたのサポーターにする  
  文章を扱う仕事や、アイデアを文章に落としてみたら、ChatGPTに入力することを検討しましょう

- 今はまだ試行錯誤の時期です  
最新情報は「いろいろ人に訊く」前に「自分で使ってみてから考える」方が良い  
  例：**ChatGPTとCopilotとGeminiの性能比較！！？** まず使ってください！！！！！！！！

- 有用なプロンプトやユースケースはそのうちアプリケーションとして提供されます  
  小難しいテクニックは「新しい技術のお試し期」である証拠



##### 今日のハンズオンどうでした？  
　　Webページが見づらい・内容が簡単すぎる/難しすぎるなど、ご意見をいただけますでしょうか🙇‍♂️