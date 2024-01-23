---
weight: 41
title: "Zero-Shotプロンプティング"
description: "Zero-shotを理解する"
icon: "step"
date: "2024-01-20T05:57:52+09:00"
lastmod: "2024-01-20T05:57:52+09:00"
draft: false
toc: true
---
{{< alert context="warning" text="このドキュメントは作成中です！👷" />}}

## 🗺️ ポイント 

Zero-shotで出力の質を向上させるプロンプト

{{< table "table-striped" >}}
| 日時 | 生成AIサービス | 共有URL |
|----------|--------------|---------|
| 2024/1/20 | ChatGPT (GPT-3.5) |aa|
{{< /table >}}


## 📃プロンプト

```
こんにちは！！今日は天気が良くて気持ちが良いです。
Take a deep breath and work on this problem step-by-step.
```
{{% alert icon="🤖" context="light" %}}
こんにちは！良い天気で気分が良い日は最高ですね。何か楽しいことをする予定がありますか？何かお手伝いできることがあれば教えてください！
{{% /alert %}}

```
こんにちは！！今日は天気が良くて気持ちが良いです。
Rephrase and expand the question and respond.
```
{{% alert icon="🤖" context="light" %}}
こんにちは！良い天気で気分が良い日は最高ですね。何か楽しいことをする予定がありますか？何かお手伝いできることがあれば教えてください！
{{% /alert %}}



## 📚 参考文献

[各種Prompt Engineeringの日本語実例集（Zero-CoT、mock、ReAct、ToT、Metacog、Step Back、IEPなど）](https://qiita.com/YutaroOgawa2/items/aca32f8fd7d551596cf8#05-zero-shot-cot-step-by-step)

[Large Language Models are Zero-Shot Reasoners](https://arxiv.org/abs/2205.11916)

https://arxiv.org/abs/2311.04205