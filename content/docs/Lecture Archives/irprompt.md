---
weight: 10
title: "MJIR2023講演"
description: "「大学IRにおける生成AI利用の試み」"
icon: "Bar_Chart"
date: "2024-01-16T09:07:27+09:00"
lastmod: "2024-01-16T09:07:27+09:00"
draft: false
toc: true
---






MJIR2023のハンズオン講演で使用したプロンプトを紹介します。

---

## 適切な生成AI利用

あまりよくない例：
```
鎌倉幕府　いつから
```

適切な使い方の一例：
```
鎌倉幕府が始まった年は1192年ではないのではないでしょうか。 
この仮説の妥当性を検証したいので、まずは別の仮説や考えを提示ください。
```




## プロンプトエンジニアリングのベストプラクティスより

### 明確な指示を書く


一例：
```
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