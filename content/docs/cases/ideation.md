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