---
weight: 68
title: "コーディングする"
description: "Excel関数・VBA・プログラミング"
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


## Excel関数の作成
---

「入力」の箇所を自由に変更してください。
```markdown
# 指示
以下の# 入力 要件を満たすExcelの関数を作成してください。

# 条件
- 関数は Excel の標準機能で実現可能なものとしてください。
- 関数名は簡潔で分かりやすいものにしてください。
- 関数の入出力パラメータは 5 個以内とし、データ型は基本的なものを使用してください。

# 入力
シート1の表とシート2の表を結合したい。
結合するキーとなる列は「個人ID」です。

# 出力
- 要件を具体的に説明し、Excel 関数作成の目的を明確にしてください。
- 関数の入出力パラメータと期待する動作を詳しく説明してください。
- 関数の使用方法は具体的な例とともに説明してください。
```

## スクリプトの作成
---

```markdown
# 以下の仕様を満たすPythonプログラムを作成してください

## 仕様
- CSVファイル `data.csv` を読み込む
- CSVファイルには `id`, `name`, `age`, `score` の4つのカラムがある
- `score` が80以上の行のみを抽出する
- 抽出した行を `id` の昇順で並べ替える
- 並べ替えた結果を `result.csv` として出力する

## 注意点
- プログラムにはコメントを付けて、処理の内容を説明してください
- 変数名やメソッド名は分かりやすい名前を使用してください
```

```markdown
jsondata=[{'metricType': 'AcademicCorporateCollaboration',  'values': [{'collabType': 'Academic-corporate collaboration',    'value': 1,    'percentage': 5},   {'collabType': 'No academic-corporate collaboration',    'value': 18,    'percentage': 94.73685}]}, {'metricType': 'AcademicCorporateCollaborationImpact',  'values': [{'collabType': 'Academic-corporate collaboration', 'value': 0.0},   {'collabType': 'No academic-corporate collaboration', 'value': 6.5}]}, {'metricType': 'Collaboration',  'values': [{'collabType': 'International collaboration', 'value': 0.0},   {'collabType': 'National collaboration', 'value': 0.9}]}, {'metricType': 'CitationCount', 'value': 117}, {'metricType': 'CitationsPerPublication', 'value': 9}, {'metricType': 'CollaborationImpact',  'values': [{'collabType': 'Institutional collaboration', 'value': 3.0},   {'collabType': 'International collaboration', 'value': 7.4},   {'collabType': 'National collaboration', 'value': 9.7},   {'collabType': 'Single authorship', 'value': 0.0}]}, {'metricType': 'CitedPublications', 'value': 14, 'percentage': 56}, {'metricType': 'FieldWeightedCitationImpact', 'value': 0.62636673}, {'metricType': 'HIndices', 'value': 15.0, 'indexType': 'h-index'}, {'metricType': 'ScholarlyOutput', 'value': 30}, {'metricType': 'PublicationsInTopJournalPercentiles',  'impactType': 'CiteScore',  'values': [{'threshold': 1, 'value': 0, 'percentage': 0.0},   {'threshold': 5, 'value': 1, 'percentage': 5.263158},   {'threshold': 10, 'value': 3, 'percentage': 15.789473},   {'threshold': 25, 'value': 10, 'percentage': 52.63158}]}, {'metricType': 'OutputsInTopCitationPercentiles',  'values': [{'threshold': 1, 'value': 0, 'percentage': 0.0},   {'threshold': 5, 'value': 0, 'percentage': 0.0},   {'threshold': 10, 'value': 0, 'percentage': 0.0},   {'threshold': 25, 'value': 4, 'percentage': 21.4}]}]
 
 
このjsondataを漏れなくパースして、dfに格納するpythonコードを書いてください
```

## GAS/VBAコードの作成
---

```markdown
# 指示
以下の作業内容を読み込み、要件に適したVBAまたはGASのコードを生成してください。

# 条件
* 複雑な操作や条件分岐がある場合は、具体的な例を挙げて説明してください。
* 特定の専門用語を使用する場合は、その定義を明確に記述してください。

# 入力
1. 対象スクリプト: VBA
2. 作業内容:
    * シート "Sheet1" の A列に入力された氏名から、敬称 ("様"、"殿" など) を削除する。
    * 処理結果は、B列に出力する。
3. 追加機能: 処理件数をログ出力する。
```


## 既存コードの解説
---

````markdown
```
import pandas as pd

df = pd.read_csv('data.csv')
filtered_df = df[df['score'] >= 80]
sorted_df = filtered_df.sort_values('id')
sorted_df.to_csv('result.csv', index=False)
```

上記のPythonプログラムに、適切なコメントを追加してください。コメントは以下の基準を満たすようにしてください。

各処理の目的や内容を簡潔に説明する
変数名やメソッド名の意味を必要に応じて説明する
コードの重要な部分や注意点を強調する
````

```markdown
以下に示すプログラミングコードを解説してください。

### 条件
* 相手は事務職員です。よってプログラミング初心者にでもわかるように解説すること。
* 一行ずつ、もしくはプログラムの意味グループずつ、丁寧に解説すること
* 基礎的な用語も懇切丁寧に説明すること
* 回答時にプログラムを出力する場合は、必ずコメントを付与すること

### プログラミングコード

// Menu sticky
function windowScroll() {
    const navbar = document.getElementById("topnav");
    if(navbar!=null){
        if (
            document.body.scrollTop >= 50 ||
            document.documentElement.scrollTop >= 50
        ) {
            navbar.classList.add("nav-sticky");
        } else {
            navbar.classList.remove("nav-sticky");
        }
    }
}

window.addEventListener('scroll', (ev) => {
    ev.preventDefault();
    windowScroll();
})

// Toggle menu
function toggleMenu() {
    document.getElementById('isToggle').classList.toggle('open');
    var isOpen = document.getElementById('navigation')
    if (isOpen.style.display === "block") {
        isOpen.style.display = "none";
    } else {
        isOpen.style.display = "block";
    }
};
```


```markdown
import pandas as pd

df = pd.read_csv('data.csv')

filtered_df = df[df['score'] >= 80]

sorted_df = filtered_df.sort_values('id')

sorted_df.to_csv('result.csv', index=False)

上記のPythonプログラムについて、コードの各部分の処理内容を解説してください。また、pandasを使用している利点についても説明してください。
```

## 既存コードの改善
---

````markdown
```
import pandas as pd

# CSVファイルを読み込む
df = pd.read_csv('data.csv')

# scoreが80以上の行を抽出する
filtered_df = df[df['score'] >= 80]

# idの昇順で並べ替える
sorted_df = filtered_df.sort_values('id')

# 結果をCSVファイルに出力する
sorted_df.to_csv('result.csv', index=False)
```

上記のPythonプログラムを改善してください。以下の点を考慮してください。

* エラー処理を追加する
* コードをより読みやすくする
* 処理速度を向上させる
````


## プログラムのエラーを読み解く
---

````markdown
```python
import pandas as pd

df = pd.read_csv('data.csv')
filtered_df = df[df['score'] > 80]
sorted_df = filtered_df.sort_values('id')
sorted_df.to_csv('result.csv')
```

上記のPythonプログラムを実行したところ、以下のエラーが発生しました。

```
Traceback (most recent call last):
  File "script.py", line 6, in <module>
    sorted_df.to_csv('result.csv')
  File "/usr/local/lib/python3.9/site-packages/pandas/core/generic.py", line 3463, in to_csv
    return DataFrameRenderer(formatter).to_csv(
  File "/usr/local/lib/python3.9/site-packages/pandas/io/formats/format.py", line 1105, in to_csv
    csv_formatter.save()
  File "/usr/local/lib/python3.9/site-packages/pandas/io/formats/csvs.py", line 241, in save
    self._save()
  File "/usr/local/lib/python3.9/site-packages/pandas/io/formats/csvs.py", line 256, in _save
    self._save_header()
  File "/usr/local/lib/python3.9/site-packages/pandas/io/formats/csvs.py", line 281, in _save_header
    writer.writerow(encoded_labels)
  File "/usr/local/lib/python3.9/site-packages/pandas/io/common.py", line 707, in writerow
    self.writer.writerow(self._encode_types(row))
UnicodeEncodeError: 'utf-8' codec can't encode characters in position 0-2: surrogates not allowed
```

このエラーの原因を特定し、修正方法を説明してください。
````

## いろんなものを変換する
---

```markdown
以下のJSONデータをPythonのデータフレームに変換し、CSVファイルとして出力するプログラムを作成してください。

{
  "employees": [
    {
      "id": 1,
      "name": "山田太郎",
      "age": 30,
      "department": "営業部"
    },
    {
      "id": 2,
      "name": "鈴木花子",
      "age": 25,
      "department": "経理部"
    },
    {
      "id": 3,
      "name": "佐藤次郎",
      "age": 35,
      "department": "営業部"
    }
  ]
}

- JSONデータは `data.json` というファイル名で保存されているとします
- 出力するCSVファイルは `employees.csv` というファイル名にしてください
- CSVファイルのヘッダーは `id`, `name`, `age`, `department` としてください
```

## 変数名・クラス名を命名する
---

```markdown
以下の仕様を満たすPythonプログラムを作成してください。

- Excelファイル `sales_data.xlsx` を読み込む
- Excelファイルには `商品ID`, `商品名`, `単価`, `数量`, `売上日` の5つのカラムがある
- `売上日` が2023年1月1日から2023年12月31日までのデータのみを抽出する
- 抽出したデータを `商品ID` と `売上日` でグループ化し、`数量` の合計を計算する
- グループ化した結果を `売上日` の昇順で並べ替える
- 並べ替えた結果を新しいExcelファイル `sales_summary.xlsx` として出力する

プログラムを作成する際、変数名やメソッド名、クラス名は適切で分かりやすい名前を使用してください。
```

## リファレンス代わりにする
---

```markdown
pandasの以下のメソッドについて説明してください。

1. read_csv()
2. groupby()
3. agg()
4. sort_values()
5. to_csv()

それぞれのメソッドについて、以下の点を説明してください。

- メソッドの目的と主な機能
- メソッドの引数とその意味
- メソッドの返り値
- メソッドの使用例
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