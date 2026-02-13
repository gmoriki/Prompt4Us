---
weight: 74
title: "コーディングする"
description: "Excel関数・Python・VBA・GAS・データ処理"
icon: "Code"
date: "2024-01-21T19:40:05+09:00"
lastmod: "2026-02-13T00:00:00+09:00"
draft: false
toc: true
---

{{< table "table-responsive" >}}
| 日時 | 使用した生成AI |
|----------|--------------|
| 2026/2/13 | ChatGPT,<br>Claude,<br>Copilot,<br>Gemini |
{{< /table >}}

## Excel関数の作成
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、2つのシートに分かれた学生データを個人IDで結合して一覧表を作りたいとき" />}}

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

{{% alert icon="🤖" context="success" %}}
**出力例**

**要件の整理**
シート1（学生基本情報）とシート2（成績情報）を「個人ID」をキーにして結合し、一つの一覧表を作成します。

**使用する関数：VLOOKUP**

シート1のA列に個人ID、B列に氏名がある場合、シート2のA列の個人IDに対応するシート1の氏名を取得するには：

```
=VLOOKUP(A2, Sheet1!A:B, 2, FALSE)
```

**引数の説明**
| 引数 | 意味 |
|------|------|
| A2 | 検索する個人ID |
| Sheet1!A:B | 検索範囲（シート1のA列〜B列） |
| 2 | 取得する列番号（2列目＝氏名） |
| FALSE | 完全一致検索 |

**注意点**
- 個人IDの表記揺れ（半角・全角）にご注意ください
- データ量が多い場合はXLOOKUP関数（Microsoft 365対応）もおすすめです
{{% /alert %}}


{{% alert icon="" context="info" %}}
以下はプログラミングの基礎知識がある方向けの内容です。
{{% /alert %}}

## スクリプトの作成
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、成績データCSVからスコア80以上の学生を抽出し、ID順に並べたリストを作成したいとき" />}}

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

{{% alert icon="🤖" context="success" %}}
**出力例**

```python
import pandas as pd

# CSVファイルを読み込む
df = pd.read_csv('data.csv')

# scoreが80以上の行のみを抽出する
high_score_df = df[df['score'] >= 80]

# idの昇順で並べ替える
sorted_df = high_score_df.sort_values('id', ascending=True)

# 結果をCSVファイルに出力する（インデックスは不要）
sorted_df.to_csv('result.csv', index=False)

print(f"抽出件数: {len(sorted_df)}件")
```

**実行方法**: ターミナルで `python script.py` を実行してください。事前に `pip install pandas` でpandasをインストールする必要があります。
{{% /alert %}}

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、名簿データから敬称を一括削除して宛名リストを整備したいとき" />}}

```markdown
以下の要件に従って、Excel VBAのコードを作成してください。

### 入力情報 ###
処理対象シート名：Sheet1

処理対象範囲：
- 入力：A列（2行目から最終行まで）
- 出力：B列（入力行に対応）

必要な機能：
- 基本機能：
  * 氏名から敬称（様、殿、さん等）を削除
  * 前後の空白を削除
  * 全角・半角の統一
  * 削除した敬称は別シートに記録

### 要件 ###
* エラーハンドリングを適切に実装する
* パフォーマンスを考慮した実装を行う
* コードの可読性を重視する
* 再利用性の高い設計にする
* 必要に応じてログ機能を実装する

### 出力形式 ###
以下の構造でコードと説明を提供します：
1. コードの概要（処理内容の説明）
2. 主要な変数・定数の説明
3. VBAコード
  - エラー処理
  - メイン処理
  - サブルーチン
4. 使用方法と注意点

### 補足 ###
* 特殊なケースの処理方法を記載
* パフォーマンスに関する注意点を説明
* 既知の制限事項がある場合は明記
```

{{% alert icon="🤖" context="success" %}}
**出力例**

**コード概要**: Sheet1のA列にある氏名から敬称を削除し、B列に出力するVBAマクロです。

```vba
Sub RemoveHonorifics()
    Dim ws As Worksheet
    Set ws = ThisWorkbook.Sheets("Sheet1")
    Dim lastRow As Long
    lastRow = ws.Cells(ws.Rows.Count, "A").End(xlUp).Row

    Dim honorifics As Variant
    honorifics = Array("様", "殿", "さん", "先生", "氏")

    Dim i As Long
    For i = 2 To lastRow
        Dim name As String
        name = Trim(ws.Cells(i, 1).Value)
        ' 敬称を削除
        Dim h As Variant
        For Each h In honorifics
            If Right(name, Len(h)) = h Then
                name = Left(name, Len(name) - Len(h))
            End If
        Next h
        ws.Cells(i, 2).Value = Trim(name)
    Next i
    MsgBox "処理完了: " & (lastRow - 1) & "件"
End Sub
```

**使用方法**: Alt+F11でVBAエディタを開き、標準モジュールに貼り付けて実行してください。
{{% /alert %}}

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、ScopusのAPIから取得したJSON形式の研究者業績データをデータフレームに変換して分析したいとき" />}}

```markdown
jsondata=[{'metricType': 'AcademicCorporateCollaboration',  'values': [{'collabType': 'Academic-corporate collaboration',    'value': 1,    'percentage': 5},   {'collabType': 'No academic-corporate collaboration',    'value': 18,    'percentage': 94.73685}]}, {'metricType': 'AcademicCorporateCollaborationImpact',  'values': [{'collabType': 'Academic-corporate collaboration', 'value': 0.0},   {'collabType': 'No academic-corporate collaboration', 'value': 6.5}]}, {'metricType': 'Collaboration',  'values': [{'collabType': 'International collaboration', 'value': 0.0},   {'collabType': 'National collaboration', 'value': 0.9}]}, {'metricType': 'CitationCount', 'value': 117}, {'metricType': 'CitationsPerPublication', 'value': 9}, {'metricType': 'CollaborationImpact',  'values': [{'collabType': 'Institutional collaboration', 'value': 3.0},   {'collabType': 'International collaboration', 'value': 7.4},   {'collabType': 'National collaboration', 'value': 9.7},   {'collabType': 'Single authorship', 'value': 0.0}]}, {'metricType': 'CitedPublications', 'value': 14, 'percentage': 56}, {'metricType': 'FieldWeightedCitationImpact', 'value': 0.62636673}, {'metricType': 'HIndices', 'value': 15.0, 'indexType': 'h-index'}, {'metricType': 'ScholarlyOutput', 'value': 30}, {'metricType': 'PublicationsInTopJournalPercentiles',  'impactType': 'CiteScore',  'values': [{'threshold': 1, 'value': 0, 'percentage': 0.0},   {'threshold': 5, 'value': 1, 'percentage': 5.263158},   {'threshold': 10, 'value': 3, 'percentage': 15.789473},   {'threshold': 25, 'value': 10, 'percentage': 52.63158}]}, {'metricType': 'OutputsInTopCitationPercentiles',  'values': [{'threshold': 1, 'value': 0, 'percentage': 0.0},   {'threshold': 5, 'value': 0, 'percentage': 0.0},   {'threshold': 10, 'value': 0, 'percentage': 0.0},   {'threshold': 25, 'value': 4, 'percentage': 21.4}]}]


このjsondataを漏れなくパースして、dfに格納するpythonコードを書いてください
```

{{% alert icon="🤖" context="success" %}}
**出力例**

```python
import pandas as pd

rows = []
for item in jsondata:
    metric = item['metricType']
    if 'values' in item:
        for v in item['values']:
            row = {'metricType': metric}
            row.update(v)
            rows.append(row)
    else:
        rows.append(item)

df = pd.DataFrame(rows)
print(df.head(10))
```

| metricType | collabType | value | percentage |
|---|---|---|---|
| AcademicCorporateCollaboration | Academic-corporate collaboration | 1 | 5.0 |
| AcademicCorporateCollaboration | No academic-corporate collaboration | 18 | 94.7 |
| ... | ... | ... | ... |
{{% /alert %}}


## 既存コードの解説
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、前任者から引き継いだPythonスクリプトの処理内容を理解するためにコメントを追加したいとき" />}}

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

{{% alert icon="🤖" context="success" %}}
**出力例**

```python
import pandas as pd  # データ分析ライブラリpandasを読み込む

# CSVファイルを読み込み、DataFrameとして格納する
df = pd.read_csv('data.csv')

# scoreが80以上の行だけを抽出する（条件フィルタリング）
filtered_df = df[df['score'] >= 80]

# id列を基準に昇順で並べ替える
sorted_df = filtered_df.sort_values('id')

# 結果をCSVファイルに出力する（index=Falseで行番号を除外）
sorted_df.to_csv('result.csv', index=False)
```
{{% /alert %}}

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、大学Webサイトのナビゲーション部分のJavaScriptコードを理解したいとき" />}}

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

{{% alert icon="🤖" context="success" %}}
**出力例**

このプログラムは、Webサイトのナビゲーションメニューの動作を制御するJavaScriptコードです。大きく2つの機能があります。

**1. スクロール時にメニューを固定する機能（Menu sticky）**

ページを50ピクセル以上下にスクロールすると、メニューバーが画面上部に固定されます。スクロール位置を元に戻すと固定が解除されます。

```javascript
// ページがスクロールされたときに呼ばれる関数
function windowScroll() {
    // "topnav"というIDのHTML要素（メニューバー）を取得する
    const navbar = document.getElementById("topnav");
    // ...
}
```

**2. ハンバーガーメニューの開閉機能（Toggle menu）**

スマートフォン等の小さい画面でメニューボタンをタップすると、メニューの表示・非表示が切り替わります。
{{% /alert %}}

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、IR部門で使われているPythonのデータ処理スクリプトの仕組みを理解したいとき" />}}

```markdown
import pandas as pd

df = pd.read_csv('data.csv')

filtered_df = df[df['score'] >= 80]

sorted_df = filtered_df.sort_values('id')

sorted_df.to_csv('result.csv', index=False)

上記のPythonプログラムについて、コードの各部分の処理内容を解説してください。また、pandasを使用している利点についても説明してください。
```

{{% alert icon="🤖" context="success" %}}
**出力例**

**各部分の処理内容**

| 行 | 処理内容 |
|---|---|
| `import pandas as pd` | pandasライブラリを`pd`という省略名で読み込みます |
| `df = pd.read_csv('data.csv')` | CSVファイルをデータフレーム（表形式のデータ）として読み込みます |
| `df[df['score'] >= 80]` | score列が80以上の行だけを抽出します |
| `.sort_values('id')` | id列を基準に昇順で並べ替えます |
| `.to_csv('result.csv', index=False)` | 結果をCSVファイルに保存します |

**pandasを使用する利点**
- Excelのような表形式データをプログラムで効率的に処理できる
- 数万行のデータでも高速に処理可能
- フィルタリング・集計・結合などの操作を簡潔なコードで記述できる
{{% /alert %}}


## 既存コードの改善
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、動作はするがエラー処理のない既存のPythonスクリプトを堅牢なコードに改善したいとき" />}}

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

{{% alert icon="🤖" context="success" %}}
**出力例**

```python
import pandas as pd
from pathlib import Path

def process_csv(input_path: str, output_path: str, min_score: int = 80):
    """CSVファイルを読み込み、条件に合うデータを抽出して出力する"""
    input_file = Path(input_path)
    if not input_file.exists():
        raise FileNotFoundError(f"入力ファイルが見つかりません: {input_path}")

    df = pd.read_csv(input_file)

    required_columns = {'id', 'name', 'age', 'score'}
    if not required_columns.issubset(df.columns):
        missing = required_columns - set(df.columns)
        raise ValueError(f"必要なカラムがありません: {missing}")

    result = (df[df['score'] >= min_score]
              .sort_values('id'))

    result.to_csv(output_path, index=False)
    print(f"処理完了: {len(result)}件を出力しました")

if __name__ == '__main__':
    process_csv('data.csv', 'result.csv')
```

**改善ポイント**: ファイル存在チェック、カラム検証、関数化による再利用性向上を行いました。
{{% /alert %}}


## プログラムのエラーを読み解く
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、CSV出力時に発生したUnicodeEncodeErrorの原因を特定し、修正方法を知りたいとき" />}}

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

{{% alert icon="🤖" context="success" %}}
**出力例**

**エラーの原因**

`UnicodeEncodeError: surrogates not allowed` は、CSVファイル内にUTF-8では表現できない不正な文字（サロゲートペア）が含まれていることが原因です。日本語の氏名データなどで、文字コードの変換ミスにより発生することがあります。

**修正方法**

```python
# 読み込み時にエンコーディングを指定する
df = pd.read_csv('data.csv', encoding='utf-8', errors='replace')

# または出力時にエラーを無視する
sorted_df.to_csv('result.csv', encoding='utf-8-sig', errors='replace')
```

**補足**: 元データがShift-JISの場合は `encoding='shift_jis'` で読み込むと解決することが多いです。大学の基幹システムから出力されるCSVはShift-JISであることが多いため、まずエンコーディングの確認をおすすめします。
{{% /alert %}}


## いろんなものを変換する
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、教務システムから出力されたJSON形式の履修登録データをCSVに変換して一覧表を作りたいとき" />}}

```markdown
以下のJSONデータをPythonのデータフレームに変換し、CSVファイルとして出力するプログラムを作成してください。

{
  "enrollments": [
    {
      "student_id": "S2024001",
      "student_name": "山田太郎",
      "course_name": "情報リテラシー",
      "faculty": "工学部"
    },
    {
      "student_id": "S2024002",
      "student_name": "鈴木花子",
      "course_name": "統計学入門",
      "faculty": "経済学部"
    },
    {
      "student_id": "S2024003",
      "student_name": "佐藤次郎",
      "course_name": "情報リテラシー",
      "faculty": "工学部"
    }
  ]
}

- JSONデータは `data.json` というファイル名で保存されているとします
- 出力するCSVファイルは `enrollments.csv` というファイル名にしてください
- CSVファイルのヘッダーは `student_id`, `student_name`, `course_name`, `faculty` としてください
```

{{% alert icon="🤖" context="success" %}}
**出力例**

```python
import json
import pandas as pd

# JSONファイルを読み込む
with open('data.json', 'r', encoding='utf-8') as f:
    data = json.load(f)

# enrollmentsキーのデータをDataFrameに変換
df = pd.DataFrame(data['enrollments'])

# CSVファイルとして出力
df.to_csv('enrollments.csv', index=False, encoding='utf-8-sig')

print(f"変換完了: {len(df)}件のデータを出力しました")
```

**出力されるCSV**
```
student_id,student_name,course_name,faculty
S2024001,山田太郎,情報リテラシー,工学部
S2024002,鈴木花子,統計学入門,経済学部
S2024003,佐藤次郎,情報リテラシー,工学部
```
{{% /alert %}}


## 変数名・クラス名を命名する
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、科研費実績データの集計プログラムを作成する際に、分かりやすい変数名・クラス名のつけ方を参考にしたいとき" />}}

```markdown
以下の仕様を満たすPythonプログラムを作成してください。

- Excelファイル `research_grant_data.xlsx` を読み込む
- Excelファイルには `課題番号`, `研究種目`, `配分額`, `採択件数`, `交付年度` の5つのカラムがある
- `交付年度` が2023年度のデータのみを抽出する
- 抽出したデータを `研究種目` と `交付年度` でグループ化し、`配分額` の合計を計算する
- グループ化した結果を `交付年度` の昇順で並べ替える
- 並べ替えた結果を新しいExcelファイル `grant_summary.xlsx` として出力する

プログラムを作成する際、変数名やメソッド名、クラス名は適切で分かりやすい名前を使用してください。
```

{{% alert icon="🤖" context="success" %}}
**出力例**

```python
import pandas as pd

# Excelファイルを読み込む
grant_data = pd.read_excel('research_grant_data.xlsx')

# 交付年度を数値型に変換
grant_data['交付年度'] = grant_data['交付年度'].astype(int)

# 2023年度のデータのみを抽出
target_year = 2023
yearly_grants = grant_data[grant_data['交付年度'] == target_year]

# 研究種目と交付年度でグループ化し、配分額を合計
grouped_summary = (yearly_grants
    .groupby(['研究種目', '交付年度'])['配分額']
    .sum()
    .reset_index())

# 交付年度の昇順で並べ替え
sorted_summary = grouped_summary.sort_values('交付年度')

# Excelファイルに出力
sorted_summary.to_excel('grant_summary.xlsx', index=False)
```

**命名のポイント**: `grant_data`（元データ）、`yearly_grants`（年度抽出）、`grouped_summary`（集計結果）、`sorted_summary`（並替済）のように、変数の内容が一目で分かる名前にしています。
{{% /alert %}}


## リファレンス代わりにする
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、pandasの主要メソッドの使い方を手軽に確認したいとき" />}}

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

{{% alert icon="🤖" context="success" %}}
**出力例**

**1. read_csv()**
- **目的**: CSVファイルをDataFrameとして読み込む
- **主な引数**: `filepath`（ファイルパス）、`encoding`（文字コード）、`header`（ヘッダー行番号）
- **返り値**: DataFrame
- **使用例**: `df = pd.read_csv('data.csv', encoding='utf-8')`

**2. groupby()**
- **目的**: 指定した列でデータをグループ化する
- **主な引数**: `by`（グループ化する列名）
- **返り値**: DataFrameGroupByオブジェクト
- **使用例**: `grouped = df.groupby('department')`

**3. agg()**
- **目的**: グループごとに集計関数を適用する
- **主な引数**: `func`（適用する関数名、辞書、リスト）
- **返り値**: DataFrame
- **使用例**: `df.groupby('department').agg({'salary': 'mean', 'age': 'max'})`

（以下、sort_values、to_csvも同様に説明が続きます）
{{% /alert %}}


## Google Formsの集計スクリプトを作成する
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、授業評価アンケートやイベント参加申込のGoogle Formsの回答をGASで自動集計したいとき" />}}

「変更箇所」を自身の状況に合わせて変更してください。

```markdown
# 指示
Google Apps Script（GAS）で以下の要件を満たすスクリプトを作成してください。

# 要件
- Google Formsの回答が記録されたスプレッドシートを対象とする
- 回答データを自動集計し、集計結果を新しいシートに出力する

# 集計内容
1. 「変更箇所：回答項目名（例：満足度）」の選択肢ごとの回答数と割合を算出
2. 「変更箇所：自由記述の項目名（例：改善点）」のテキスト回答一覧を作成
3. 回答の日別推移を集計

# スプレッドシートの構造
- 「変更箇所：シート名（例：フォームの回答 1）」シートに回答データが格納されている
- A列: タイムスタンプ
- B列: 「変更箇所：項目名（例：所属学部）」
- C列: 「変更箇所：項目名（例：満足度）」（5段階評価）
- D列: 「変更箇所：項目名（例：改善点についてのご意見）」（自由記述）

# 条件
- コードにはコメントを付けて処理内容を説明すること
- エラーハンドリングを適切に実装すること
- 集計結果シートが既に存在する場合は上書きすること
```

{{% alert icon="🤖" context="success" %}}
**出力例**

```javascript
function aggregateFormResponses() {
  const ss = SpreadsheetApp.getActiveSpreadsheet();
  const sourceSheet = ss.getSheetByName('フォームの回答 1');
  const data = sourceSheet.getDataRange().getValues();
  const headers = data[0];
  const responses = data.slice(1);

  // 集計結果シートを作成（既存の場合は削除して再作成）
  let resultSheet = ss.getSheetByName('集計結果');
  if (resultSheet) ss.deleteSheet(resultSheet);
  resultSheet = ss.insertSheet('集計結果');

  // 満足度の集計（C列）
  const satisfactionCounts = {};
  responses.forEach(row => {
    const val = row[2];
    satisfactionCounts[val] = (satisfactionCounts[val] || 0) + 1;
  });

  resultSheet.getRange('A1').setValue('【満足度集計】');
  resultSheet.getRange('A2:C2').setValues([['評価', '回答数', '割合']]);
  let rowIndex = 3;
  for (const [key, count] of Object.entries(satisfactionCounts)) {
    const percentage = (count / responses.length * 100).toFixed(1);
    resultSheet.getRange(rowIndex, 1, 1, 3)
      .setValues([[key, count, percentage + '%']]);
    rowIndex++;
  }

  SpreadsheetApp.getUi().alert('集計が完了しました');
}
```

**使い方**: スプレッドシートの「拡張機能」→「Apps Script」からスクリプトを貼り付けて実行します。初回実行時にスプレッドシートへのアクセス許可が求められます。
{{% /alert %}}


## 業務自動化スクリプトを作成する
---

{{< alert context="info" text="**対象: 全職種共通**<br>**想定シーン**: 大学職員が、フォルダ内の大量のファイルを命名規則に従ってリネーム・整理したいとき" />}}

「変更箇所」を自身の状況に合わせて変更してください。

```markdown
# 指示
以下の業務を自動化するPythonスクリプトを作成してください。

# 自動化したい業務
「変更箇所：自動化したい業務内容（例：フォルダ内のファイルを命名規則に従ってリネームする）」

# 現在の手作業の流れ
1. 「変更箇所：手順1（例：ダウンロードフォルダから対象ファイルを探す）」
2. 「変更箇所：手順2（例：ファイル名を「日付_カテゴリ_連番」の形式に変更する）」
3. 「変更箇所：手順3（例：カテゴリ別のフォルダに移動する）」

# 条件
- Pythonの標準ライブラリのみで動作すること（追加インストール不要）
- 実行前に処理対象ファイルの一覧を表示し、確認を求めること
- 処理ログをテキストファイルに出力すること
- エラーが発生しても他のファイルの処理を継続すること

# 対象ファイル
- 「変更箇所：対象フォルダのパス（例：C:\Users\担当者\Downloads）」
- 「変更箇所：対象ファイルの拡張子（例：.pdf, .xlsx）」
```

{{% alert icon="🤖" context="success" %}}
**出力例**

```python
import os
import shutil
import datetime
import re

def organize_files(source_dir, target_dir):
    """ファイルを命名規則に従ってリネーム・整理する"""
    log_entries = []
    today = datetime.date.today().strftime('%Y%m%d')

    # 対象ファイルの一覧を取得
    target_extensions = ('.pdf', '.xlsx')
    files = [f for f in os.listdir(source_dir)
             if os.path.isfile(os.path.join(source_dir, f))
             and f.lower().endswith(target_extensions)]

    if not files:
        print("対象ファイルがありません。")
        return

    # 処理対象の確認
    print(f"対象ファイル: {len(files)}件")
    for f in files:
        print(f"  - {f}")
    confirm = input("\n処理を実行しますか？ (y/n): ")
    if confirm.lower() != 'y':
        print("処理を中止しました。")
        return

    # ファイルをリネーム・移動
    for i, filename in enumerate(files, 1):
        try:
            ext = os.path.splitext(filename)[1]
            new_name = f"{today}_資料_{i:03d}{ext}"
            src = os.path.join(source_dir, filename)
            dst = os.path.join(target_dir, new_name)
            shutil.move(src, dst)
            log_entries.append(f"[成功] {filename} -> {new_name}")
        except Exception as e:
            log_entries.append(f"[エラー] {filename}: {e}")

    # ログ出力
    log_path = os.path.join(target_dir, f"処理ログ_{today}.txt")
    with open(log_path, 'w', encoding='utf-8') as f:
        f.write('\n'.join(log_entries))

    print(f"\n処理完了。ログ: {log_path}")

if __name__ == '__main__':
    organize_files('./Downloads', './整理済み')
```

**使い方**: フォルダパスを実際の環境に合わせて変更し、ターミナルで `python organize_files.py` を実行してください。処理前に確認プロンプトが表示されるため、誤操作の心配がありません。
{{% /alert %}}
