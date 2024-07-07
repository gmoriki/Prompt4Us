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
