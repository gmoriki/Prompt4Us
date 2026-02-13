---
weight: 63
title: "アイデアを出す"
description: "企画立案・命名・ブレスト・仮説整理"
icon: "Lightbulb"
date: "2024-01-21T19:45:42+09:00"
lastmod: "2026-02-13T00:00:00+09:00"
draft: false
toc: true
---

企画のタネを出したいとき、名前を考えたいとき、仮説を整理したいとき――AIを「壁打ち相手」にして、アイデアを広げたり磨いたりするためのプロンプト集です。

## 施設の名前を決める
---

{{< alert context="info" text="**想定シーン**: 大学のキャンパスに新設された共有スペースの名称を決めたい。候補を複数出して関係者で検討したい。" />}}

「要件」を自身の状況に合わせて変更してください。

```markdown
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
**出力例**

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

## 企画案の典型を出す
---

{{< alert context="info" text="**想定シーン**: 大学職員向けの勉強会を企画したい。アンケート結果をもとに、トレンドを踏まえたテーマ候補をAIに提案してもらう。" />}}

「関心事項・課題」を自身の状況に合わせて変更してください。

```markdown
大学職員向けの勉強会のテーマを設定したいです。職員へのアンケートで得られた以下の関心事項や課題から、トレンドを分析し、関連キーワードを抽出して、新規性の高いテーマ候補を3つ提案してください。

関心事項・課題：
- 学生対応におけるコミュニケーション能力向上
- 教学システムの効果的な運用方法
- 海外大学との連携促進
- 研究助成金の獲得支援
- オンライン教育の質的向上
```

{{% alert icon="🤖" context="success" %}}
**出力例**

**トレンド分析と関連キーワード**

アンケート結果からは「学生中心の対応力強化」「デジタル活用の深化」「グローバル化への対応」の3軸が浮かび上がります。

**テーマ候補**

1. **「AI時代の学生コミュニケーション ── チャットボット活用と対面対応のベストミックス」**
   - 関連キーワード：生成AI、チャットボット、学生満足度、ハイブリッド対応
   - 新規性：デジタルと対面を組み合わせた対応モデルを職員自身が設計する実践型ワークショップ

2. **「教学IRデータを活かした学修成果の可視化と改善サイクル」**
   - 関連キーワード：教学IR、ラーニングアナリティクス、PDCA、エビデンスベースド
   - 新規性：既存の教学システムから得られるデータを分析し、具体的な改善アクションにつなげる手法を学ぶ

3. **「海外大学連携×オンライン教育 ── COIL型学習プログラムの設計と運用」**
   - 関連キーワード：COIL、バーチャル交換留学、国際連携、オンライン協働学習
   - 新規性：渡航を伴わない国際連携モデルを職員主導で構築するためのノウハウを共有する

{{% /alert %}}

## キャッチコピーの作成
---

{{< alert context="info" text="**想定シーン**: 大学の広報担当が、新しい学部やイベントのキャッチコピーを考えたい。ターゲットやブランドトーンを指定して候補を生成する。" />}}

「target_audience」「product_description」「brand_tone」の箇所を自由に変更してください。

```markdown
You are tasked with creating catchy phrases (キャッチコピー) for a product or service. Your goal is to craft memorable and impactful phrases that will resonate with the target audience and effectively communicate the product's key benefits or features.

You will be provided with the following information:

<target_audience>
{{TARGET_AUDIENCE}}
</target_audience>

<product_description>
{{PRODUCT_DESCRIPTION}}
</product_description>

<brand_tone>
{{BRAND_TONE}}
</brand_tone>

Analyze the provided information carefully. Consider the target audience's characteristics, needs, and preferences. Understand the product's unique selling points and key features. Pay attention to the brand's tone and ensure your phrases align with it.

When creating catchy phrases, keep the following guidelines in mind:
1. Be concise and impactful - aim for phrases that are short but memorable
2. Highlight the product's unique selling points or benefits
3. Use language that resonates with the target audience
4. Incorporate wordplay, rhymes, or alliteration when appropriate
5. Ensure the phrases are easy to understand and remember
6. Align the tone and style with the brand's image

Generate 5 catchy phrases in Japanese. For each phrase, provide a brief explanation (in Japanese) of why it's effective and how it relates to the product and target audience.

Present your output in the following format:

<catchphrase_list>
<catchphrase>
<phrase>[Catchy phrase in Japanese]</phrase>
<explanation>[Brief explanation in Japanese]</explanation>
</catchphrase>
[Repeat for all 5 phrases]
</catchphrase_list>

Remember to be creative and think from the perspective of the target audience. Your goal is to create phrases that will grab attention and leave a lasting impression.
```

{{% alert icon="🤖" context="success" %}}
**出力例**（TARGET_AUDIENCE=高校生、PRODUCT_DESCRIPTION=データサイエンス学部、BRAND_TONE=先進的で親しみやすい の場合）

<catchphrase_list>
<catchphrase>
<phrase>データで未来を描こう。</phrase>
<explanation>高校生に「自分の手で未来を切り拓ける」というメッセージを伝え、データサイエンスの可能性を直感的に表現しています。</explanation>
</catchphrase>
<catchphrase>
<phrase>好奇心、数字に変えよう。</phrase>
<explanation>「好奇心」という高校生に身近な感情を起点にし、データサイエンスとの接点を自然につくっています。</explanation>
</catchphrase>
<catchphrase>
<phrase>答えのない問いに、データという翼を。</phrase>
<explanation>探究学習に親しんだ高校生に響くフレーズ。学部で得られるスキルを「翼」というポジティブなイメージで表現しています。</explanation>
</catchphrase>
<catchphrase>
<phrase>世界を読み解くチカラ、ここから。</phrase>
<explanation>「ここから」という言葉で入学への後押しをしつつ、データリテラシーの価値を端的に伝えています。</explanation>
</catchphrase>
<catchphrase>
<phrase>キミの「なぜ？」がイノベーションになる。</phrase>
<explanation>高校生の日常的な疑問をイノベーションにつなげるストーリーを1文で描き、親しみやすさと先進性を両立しています。</explanation>
</catchphrase>
</catchphrase_list>

{{% /alert %}}

## 記事タイトルの作成
---

{{< alert context="info" text="**想定シーン**: 大学のブログやニュースレターの記事タイトルを考えたい。Fewshotで論点を整理しながら、キャッチーなタイトルをAIに考案してもらう。" />}}

引用元：[AI時代の質問力 プロンプトリテラシー 「問い」と「指示」が生成AIの可能性を最大限に引き出す](https://www.shoeisha.co.jp/book/detail/9784798188102)

Fewshotで論点を整理した上で、ブログタイトルを考案するプロンプトです。

最後の「内容」の個所を自由に変更してください。

```markdown
内容：OpenAIのChatGPTが人々の仕事を奪う可能性に関するブログ記事

論点：一体、何の話題か、
出力：AIの進化

論点：最も大事なニュースはなにか、
出力：ChatGPTは私たちの仕事を奪うか否か

論点：最大30字程度のタイトルを考える、
出力：AIの進化：ChatGPTは我々の仕事を奪うか？

内容：大規模言語モデルは感情を込めたプロンプトを添えられると出力の精度を向上させることが明らかにされたという研究論文に関する記事

論点：一体、何の話題か、
出力：大規模言語モデルのプロンプト

論点：最も大事なニュースはなにか、
出力：感情をプロンプトに添えると大規模言語モデルの精度が向

論点：最大30字程度のタイトルを考える
出力：感情プロンプトでAI精度向上の展望

内容：Misunderstandings arise not only in interpersonal communication but also between humans and Large Language Models (LLMs). Such discrepancies can make LLMs interpret seemingly unambiguous questions in unexpected ways, yielding incorrect responses. While it is widely acknowledged that the quality of a prompt, such as a question, significantly impacts the quality of the response provided by LLMs, a systematic method for crafting questions that LLMs can better comprehend is still underdeveloped. In this paper, we present a method named `Rephrase and Respond' (RaR), which allows LLMs to rephrase and expand questions posed by humans and provide responses in a single prompt. This approach serves as a simple yet effective prompting method for improving performance. We also introduce a two-step variant of RaR, where a rephrasing LLM first rephrases the question and then passes the original and rephrased questions together to a different responding LLM. This facilitates the effective utilization of rephrased questions generated by one LLM with another. Our experiments demonstrate that our methods significantly improve the performance of different models across a wide range to tasks. We further provide a comprehensive comparison between RaR and the popular Chain-of-Thought (CoT) methods, both theoretically and empirically. We show that RaR is complementary to CoT and can be combined with CoT to achieve even better performance. Our work not only contributes to enhancing LLM performance efficiently and effectively but also sheds light on a fair evaluation of LLM capabilities. Data and codes are available at this https URL.
論点：
```

{{% alert icon="🤖" context="success" %}}
**出力例**

論点：一体、何の話題か、
出力：LLMのプロンプト改善手法

論点：最も大事なニュースはなにか、
出力：質問を言い換えるだけでAIの回答精度が向上する新手法「RaR」

論点：最大30字程度のタイトルを考える
出力：「質問の言い換え」でAI精度が劇的に向上

{{% /alert %}}

## AIに質問してもらう
---

{{< alert context="info" text="**想定シーン**: 学生の思考力を引き出す授業設計のヒントを得たい。ソクラテス・メソッドをAIに実践させ、対話の進め方を体験する。" />}}

ソクラテスメソッドによる議論の深化。「入力文」を自身の状況に合わせて変更してください。

```markdown
以下の入力文は、大学生が知りたい・言語化したい概念やキーワードです。入力文に対してソクラテス・メソッドを活用し、学習者が解を言語化するまで、献身的なサポートを続けてください。

### 条件
* あなたは、常にソクラテススタイルで対応する家庭教師です。
* 生徒に答えを与えるのではなく、生徒が自分で考える力を身につけるために、常に適切な質問をするようにします。
* 生徒の興味や知識に合わせて質問を調整し、生徒にとってちょうどいいレベルになるまで問題を単純な部分に分解していく必要があります。

### 入力文
大学における教育と研究の関係について
```

{{% alert icon="🤖" context="success" %}}
**出力例**

とても興味深いテーマですね。一緒に考えていきましょう。

まず基本的なところから確認させてください。

**あなたにとって「教育」とは何をすることだと思いますか？** 自分の言葉で構いませんので、思いつくままに答えてみてください。

（ここから対話が続き、学習者の回答に応じて次の問いが生成されます。例えば「教育は知識を伝えること」と答えると、「では研究はどのような活動でしょうか？」「教育と研究で共通している部分はありますか？」と段階的に深まっていきます。）

{{% /alert %}}

## 仮説を形成する
---

{{< alert context="info" text="**想定シーン**: 大学業務の課題について自分なりの仮説を持っているが、視野が狭くなっていないか心配。AIに批判的・建設的に分析してもらい、仮説をブラッシュアップしたい。" />}}

「仮説」を自身の状況に合わせて変更してください。

```markdown
次の2ステップで、私の仮説を改善してください。

### 仮説 ###
大学業務が問題を抱えるの全ての原因は〇〇である

### ステップ ###
- 仮説の特長を批判的かつ建設的に分析する
- 明るい未来をつくるための提言に言い換える
```

{{% alert icon="🤖" context="success" %}}
**出力例**（仮説：「大学業務が問題を抱える全ての原因は縦割り組織である」の場合）

#### ステップ1：批判的かつ建設的な分析

**仮説の強み：**
- 縦割り組織は多くの大学で実際に課題として認識されており、問題意識として妥当性がある
- 部署間連携の不足が業務効率に影響するという指摘は、実務経験に裏打ちされた洞察

**仮説の課題：**
- 「全ての原因」という表現は過度な一般化。予算制約・人材不足・制度的要因など他の構造的要因を見落とす恐れがある
- 「縦割り」の定義が曖昧で、組織構造の問題なのか、文化・慣習の問題なのか区別がつかない
- 縦割り組織にも専門性の深化や責任の明確化といったメリットがある

#### ステップ2：提言への言い換え

**改善後の仮説：**
「大学業務の多くの課題は、部署間の情報共有と協働の仕組みが不十分であることに起因している。縦割り構造の専門性を活かしつつ、横断的なプロジェクト体制や定期的な部署間対話の場を設けることで、業務品質と職員の働きがいの両方を向上させることができる。」

{{% /alert %}}

## 仮説を反復的に改善する
---

{{< alert context="info" text="**想定シーン**: AIとの対話で得られた回答をさらに深掘りしたい。建設的・批判的な観点から反復的に改善し、アイデアの完成度を高める。" />}}

既にAIから得られた回答に対して、以下のプロンプトを続けて投げかけてください。

```markdown
以上の主張を建設的かつ批判的観点から改善しましょう。

1.  改善すればもっと良くなる点、意味がはっきりしていない点、課題などを5つあげる
2. 1.で挙げた点に基づき、修正点を5つ挙げる
3. ダイアグラムダイアグラムを積極的・抜本的に修正し、出力する
4. 1.から3.を3回繰り返す
```

{{% alert icon="🤖" context="success" %}}
**出力例**

#### 反復1回目

**1. 改善点の指摘**
1. 「業務効率化」の定義が曖昧 ── 何をもって効率化とするか、定量的な指標が必要
2. ステークホルダーの範囲が不明確 ── 教員・職員・学生のどこまでを対象とするか
3. 実施スケジュールの現実性 ── 年度途中の導入は予算・人員の制約がある
4. 成功指標（KPI）が設定されていない
5. 類似施策との差別化ポイントが弱い

**2. 修正点**
1. 効率化の定義を「処理時間の20%削減」など具体化
2. 対象を「教務課職員」に限定して段階的に拡大
3. パイロット期間を設け、次年度本格導入とする
4. 月次レビューでKPIを確認するPDCAサイクルを組み込む
5. 先行大学の事例を参照し差別化要素を明記

**3. 修正後のダイアグラム**
（改善された構造図が出力されます）

*以降、2回目・3回目の反復でさらに精緻化されていきます。*

{{% /alert %}}

## アイデアを自由に吐露する
---

{{< alert context="info" text="**想定シーン**: 頭の中にぼんやりあるアイデアを言語化して、AIに壁打ち相手になってもらいたい。まずは気軽に投げかけてフィードバックをもらう。" />}}

思いついたアイデアをそのままAIに投げかけてみましょう。整理されていなくても大丈夫です。

```markdown
生成AIに対する注意喚起を出した大学一覧をgoogle spreadシートにまとめて公開しています。これをDBで管理・公表したほうがいいインセンティブはある？
```

{{% alert icon="🤖" context="success" %}}
**出力例**

面白い着眼点ですね。Google SpreadsheetからDB管理に移行するインセンティブについて、いくつかの観点から整理してみます。

**DB化のメリット**
- **検索性の向上：** 大学名・発表時期・方針内容などで柔軟にフィルタリングできる
- **データの一貫性：** 入力フォーマットを統一し、表記ゆれや重複を防止できる
- **API連携の可能性：** 他のサービスや研究者が自動でデータを取得・分析できる
- **更新履歴の管理：** いつ・誰が・何を更新したかを正確に追跡できる

**一方で考慮すべき点**
- **運用コスト：** DB構築・サーバー維持の手間と費用がかかる
- **Spreadsheetの手軽さ：** 現状のシート共有で十分にニーズを満たしている可能性
- **コントリビュータの参入障壁：** DB化すると気軽に情報追加しにくくなるかもしれない

**提案：** まずはスプレッドシートの構造化（列の定義統一）から始め、利用者が増えてきたらNotion DBやAirtableなどの中間的なツールを検討するのはいかがでしょうか？

{{% /alert %}}

## イベント企画を立案する
---

{{< alert context="info" text="**想定シーン**: FD/SD研修やオープンキャンパスなど、大学で開催するイベントの企画案を検討したい。AIに壁打ちしながらアイデアを広げる。" />}}

「変更箇所」を自身の状況に合わせて変更してください。

```markdown
あなたは大学のイベント企画の壁打ち相手です。
以下の情報をもとに、イベントの企画案を3つ提案してください。

### イベント情報 ###
- イベント種別：SD研修（職員向け能力開発）
- テーマ：生成AIの業務活用
- 対象者：大学職員（事務系）約30名
- 時間：2時間
- 会場：学内の中規模会議室（PC持ち込み可）
- 予算：5万円以内（外部講師費用は別途）
- 制約：参加者のITリテラシーにばらつきがある

### 出力形式 ###
各企画案について以下を含めてください：
- 企画タイトル
- コンセプト（1〜2文）
- タイムスケジュール（大まかな時間配分）
- 必要な準備物
- 期待される成果
- リスクと対策
```

{{% alert icon="🤖" context="success" %}}
**出力例**

#### 企画案1：「はじめての生成AI ── 明日から使える業務効率化ワークショップ」

**コンセプト：** ITリテラシーの差を前提に、全員が「自分の業務で使えた」という成功体験を持ち帰れるハンズオン型研修。

**タイムスケジュール：**
| 時間 | 内容 |
|------|------|
| 0:00-0:20 | イントロ：生成AIとは何か（デモ中心） |
| 0:20-0:50 | ハンズオン1：メール文面作成・要約を体験 |
| 0:50-1:00 | 休憩 |
| 1:00-1:30 | ハンズオン2：自分の業務課題でプロンプトを作成 |
| 1:30-1:50 | グループ共有：うまくいったプロンプトを発表 |
| 1:50-2:00 | まとめ・振り返りアンケート |

**必要な準備物：** Wi-Fi環境、スクリーン、参加者用ハンドアウト（プロンプト例集）
**期待される成果：** 参加者全員が少なくとも1つ、自業務に使えるプロンプトを作成できる
**リスクと対策：** ネットワーク不調 → モバイルWi-Fiをバックアップとして用意

（以下、企画案2・3が続きます）

{{% /alert %}}

## SWOT分析で施策を検討する
---

{{< alert context="info" text="**想定シーン**: 大学や部署の強み・弱み・機会・脅威を整理して、具体的な施策アイデアを出したい。AIにSWOT分析のフレームワークで思考を支援してもらう。" />}}

「変更箇所」を自身の状況に合わせて変更してください。

```markdown
以下の情報をもとに、SWOT分析を行い、クロスSWOT分析から具体的な施策アイデアを5つ提案してください。

### 分析対象 ###
大学の入試広報戦略

### SWOT要素 ###
#### 強み (Strengths)
- 地域密着型の教育で就職率が高い
- 少人数教育によるきめ細かな指導

#### 弱み (Weaknesses)
- 全国的な知名度が低い
- SNSやデジタルマーケティングのノウハウが不足

#### 機会 (Opportunities)
- 地方創生への社会的関心の高まり
- オンラインでの大学説明会が一般化

#### 脅威 (Threats)
- 18歳人口の減少
- 都市部大学との競争激化

### 出力形式 ###
1. SWOT分析の整理表
2. クロスSWOT分析（強み×機会、強み×脅威、弱み×機会、弱み×脅威）
3. 各象限から導かれる施策アイデア（計5つ以上）
```

{{% alert icon="🤖" context="success" %}}
**出力例**

#### 1. SWOT分析の整理表

| | プラス要因 | マイナス要因 |
|---|---|---|
| **内部環境** | 高い就職率、少人数教育 | 知名度不足、デジタルマーケティング力不足 |
| **外部環境** | 地方創生への関心、オンライン説明会の一般化 | 18歳人口減少、都市部大学との競争 |

#### 2. クロスSWOT分析

**強み × 機会（積極戦略）：** 高い就職率と地方創生を掛け合わせ、「地域で活躍する卒業生」のストーリーをオンライン説明会で発信
**強み × 脅威（差別化戦略）：** 少人数教育を武器に、都市部大学にはできない「一人ひとりに寄り添うサポート」を前面に打ち出す
**弱み × 機会（改善戦略）：** オンライン説明会の一般化を契機に、低コストでデジタルマーケティングのスキルを獲得する
**弱み × 脅威（防衛戦略）：** 知名度不足×人口減少に対し、特定地域・特定層にターゲットを絞った効率的な広報に転換

#### 3. 施策アイデア

1. **卒業生インタビュー動画シリーズ** ── 地元企業で活躍する卒業生を取材し、SNSとオンライン説明会で配信
2. **高校教員向けオンライン大学見学会** ── 少人数ゼミの様子をライブ配信し、教育の質を体感してもらう
3. **地方創生プロジェクト発表会の公開** ── 学生の地域連携活動を外部公開し、大学の存在感を高める
4. **SNS運用チームの立ち上げ** ── 学生広報スタッフを募集し、若い感性でのデジタル発信力を強化
5. **ターゲットエリア集中広報** ── 通学圏内の高校に絞り、出張講義やミニ説明会を重点実施

{{% /alert %}}

## ブレインストーミングを構造化する
---

{{< alert context="info" text="**想定シーン**: あるテーマについてアイデアを量産したいが、発散しすぎて収拾がつかなくなりがち。制約条件を設定してAIにブレストを構造化してもらう。" />}}

「変更箇所」を自身の状況に合わせて変更してください。

```markdown
以下のテーマについて、構造化されたブレインストーミングを行ってください。

### テーマ ###
大学の窓口業務のデジタル化

### 制約条件 ###
- 予算：年間100万円以内
- 期間：1年以内に導入可能
- 前提：既存の学務システム（教務システム・ポータル）は変更しない
- 対象：学生からの問い合わせ対応（証明書発行、履修相談、施設予約など）

### ブレスト方法 ###
1. まず制約を無視してアイデアを20個出す（量重視）
2. 制約条件でフィルタリングし、実現可能なアイデアを10個に絞る
3. 絞ったアイデアを「効果の大きさ」と「導入の容易さ」で2軸マトリクスに分類する
4. 最優先で取り組むべきアイデアTOP3を選び、それぞれ簡単な実施計画を添える
```

{{% alert icon="🤖" context="success" %}}
**出力例**

#### 1. アイデア出し（20個・制約無視）

1. AIチャットボットで24時間対応
2. LINEで問い合わせ受付
3. FAQ自動生成システム
4. 証明書のオンライン申請・コンビニ発行
5. 予約システムの導入（窓口来訪予約）
6. ビデオ通話での遠隔窓口
...（20個まで続く）

#### 2. 制約条件フィルタリング後（10個）

（予算・期間・既存システム維持の観点でフィルタリング）

#### 3. 2軸マトリクス

|  | 導入が容易 | 導入に手間がかかる |
|---|---|---|
| **効果大** | FAQ整備+チャットボット、窓口予約システム | LINE連携、証明書オンライン申請 |
| **効果中** | 問い合わせフォーム統一、対応マニュアル整備 | ビデオ通話窓口 |

#### 4. 最優先TOP3

**1位：FAQ整備+簡易チャットボット導入**
- 実施計画：過去の問い合わせデータを分析 → FAQ作成 → 無料/低コストのチャットボットツールで実装
- 期間：3か月、費用：約20万円

**2位：窓口来訪予約システム**
- 実施計画：Google FormsやMicrosoft Bookingsなど既存ツールを活用
- 期間：1か月、費用：ほぼゼロ

**3位：問い合わせフォームの統一・整理**
- 実施計画：各課で散在するフォームをポータルに集約し、カテゴリ別に整理
- 期間：2か月、費用：約10万円

{{% /alert %}}
