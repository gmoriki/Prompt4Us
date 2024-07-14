---
weight: 62
title: "アイデアを出す"
description: "施設名・企画案・コピー"
icon: "article"
date: "2024-01-21T19:45:42+09:00"
lastmod: "2024-01-21T19:45:42+09:00"
draft: false
toc: true
---

{{< table "table-responsive" >}}
| 日時 | 使用した生成AI | 
|----------|--------------|
| 2024/7/7 | ChatGPT(GPT-3.5),<br>Claude(3.5 Sonnet),<br>Copilot(GPT-4) |
{{< /table >}}


## 施設の名前を決める
---

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

```markdown
大学職員向けの勉強会のテーマを設定したいです。職員へのアンケートで得られた以下の関心事項や課題から、トレンドを分析し、関連キーワードを抽出して、新規性の高いテーマ候補を3つ提案してください。
 
関心事項・課題：
- 学生対応におけるコミュニケーション能力向上
- 教学システムの効果的な運用方法
- 海外大学との連携促進
- 研究助成金の獲得支援
- オンライン教育の質的向上
```

## キャッチコピーの作成
---

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

## 記事タイトルの作成
---

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

## AIに質問してもらう
---

ソクラテスメソッドによる議論の深化
```markdown
以下の入力文は、大学生が知りたい・言語化したい概念やキーワードです。入力文に対してソクラテス・メソッドを活用し、学習者が解を言語化するまで、献身的なサポートを続けてください。

### 条件
* あなたは、常にソクラテススタイルで対応する家庭教師です。
* 生徒に答えを与えるのではなく、生徒が自分で考える力を身につけるために、常に適切な質問をするようにします。
* 生徒の興味や知識に合わせて質問を調整し、生徒にとってちょうどいいレベルになるまで問題を単純な部分に分解していく必要があります。

### 入力文
大学における教育と研究の関係について
```

