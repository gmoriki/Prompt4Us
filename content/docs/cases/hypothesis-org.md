---
weight: 66
title: "仮説を整理する"
description: "整理・分類・繰り返し処理"
icon: "article"
date: "2024-01-21T19:40:49+09:00"
lastmod: "2024-01-21T19:40:49+09:00"
draft: false
toc: true
---

{{< table "table-responsive" >}}
| 日時 | 使用した生成AI | 
|----------|--------------|
| 2024/7/7 | ChatGPT(GPT-3.5),<br>Claude(3.5 Sonnet),<br>Copilot(GPT-4) |
{{< /table >}}

## 仮説を形成する
---

```markdown
次の2ステップで、私の仮説を改善してください。

### 仮説 ###
大学業務が問題を抱えるの全ての原因は〇〇である

### ステップ ###
- 仮説の特長を批判的かつ建設的に分析する
- 明るい未来をつくるための提言に言い換える
```

## 仮説を形成する(2)
---

※既に得られた回答に対するプロンプト
```markdown
以上の主張を建設的かつ批判的観点から改善しましょう。

1.  改善すればもっと良くなる点、意味がはっきりしていない点、課題などを5つあげる
2. 1.で挙げた点に基づき、修正点を5つ挙げる
3. ダイアグラムダイアグラムを積極的・抜本的に修正し、出力する
4. 1.から3.を3回繰り返す
```
## 仮説を形成する(3)
---

弁証法的エンジン
```markdown
You are tasked with engaging in a dialectical process of thesis, antithesis, and synthesis. This process will be repeated five times, starting with an initial claim and progressively refining it through criticism and synthesis.
Here is the initial claim:

大学事務における人事異動は不要である

For each iteration, follow these steps:

Criticism (Antithesis):
Generate a thoughtful criticism or counterargument to the current claim. This criticism should challenge the claim's assumptions, point out potential flaws, identify hidden premises, or present alternative viewpoints. The criticism should be multifaceted and thorough in its logical analysis.
Synthesis:
Create a new claim that addresses the criticism while preserving the valuable aspects of the original claim. This synthesis should represent a more refined and nuanced position that takes both the original claim and the criticism into account.

Repeat this process five times, with each new synthesis becoming the claim for the next iteration.
Present your output in the following format:
Iteration 1
Criticism
[Your multifaceted criticism here]
Synthesis
[Your synthesis here]
Iteration 2
[Continue for iterations 2, 3, 4, and 5]
Ensure that each iteration builds upon the previous one, gradually refining and improving the claim through the dialectical process.
回答は日本語でお願いします
```

## 自身の気持ちを吐露する
---
```markdown
無条件に褒めてくれ〜〜でも無理に頑張れと言って私を鼓舞させるのではなく、ありのままの私を認めてほしい。あなたの回答の一言一句が私の労働生産性に直結します。
```

## 自身のアイデアを吐露する
---

```markdown
生成AIに対する注意喚起を出した大学一覧をgoogle spreadシートにまとめて公開しています。これをDBで管理・公表したほうがいいインセンティブはある？
```

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