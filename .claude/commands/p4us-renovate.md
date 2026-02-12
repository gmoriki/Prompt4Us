# P4Us改修スキル

P4Us（Prompt Guide for University staff）の改修を行う際に従うべき方法論とコンテキスト。

## P4Usの理念（最重要）

改修の前に必ずこの理念を理解し、すべての変更がこれと整合することを確認する。

- **「固すぎず柔らかすぎない」「難しすぎず易しすぎない」** 情報整備
- プロンプトは「呪文」ではなく **「依頼文」**
- AIは「賢い辞書」ではなく **「考えを壁打ちできる相棒」**
- 「適切な扱い方 → 上手な扱い方」の順序を大切にする
- P4Usは「プロンプトガイド」だが、実態は **生成AI利用リテラシーガイド**（55%がリテラシー/マインドセット/付き合い方）

## 改修の進め方

### Phase 1: 調査・現状把握（Plan Mode）

1. **EnterPlanMode** を使い、まず計画を立てる
2. **Explore エージェント**を並列で起動し、以下を調査:
   - サイト全体のファイル構成・lastmod・weight順序
   - 壊れたリンク・古いモデル名・残存マーカー
   - コンテンツ品質（薄いページ、出力例の有無）
3. 調査結果を統合し、変更対象を **カテゴリ分け** する:
   - カテゴリA: 機械的修正（404、typo、マーカー削除等）
   - カテゴリB: 普遍化（モデル名のバージョン番号除去等）
   - カテゴリC: コンテンツ品質改善（議論が必要）
   - カテゴリD: スコープ判断が必要（チームで議論）

### Phase 2: 実装（Agent Teams）

大規模改修の場合は **TeamCreate** でチームを組む:

| 役割 | エージェント | 担当 |
|------|------------|------|
| reviewer | general-purpose | 品質レビュー・方針議論リード |
| mechanic | general-purpose | 機械的修正・普遍化 |
| writer | general-purpose | コンテンツ執筆 |

- **mechanic** はカテゴリA/Bを先行実施（議論不要）
- **writer** と **reviewer** はカテゴリC/Dを議論→執筆→レビューの流れで進行
- 全員が SendMessage で連携し、相互レビューを行う

### Phase 3: 戦略的更新

新コンテンツの追加や大きな方針変更を伴う場合:

1. **Explore エージェント**で外部動向リサーチ（Web検索含む）
2. **著者の思想分析**（note記事、speakerdeck、researchmap等）
3. **サイト内部の理念分析**（how-to-use.md、ai-partnership.md等がコア）
4. 3つの調査を統合し、**理念ドリブンで** 方針を決定
5. 変更は最小限に。P4Usの既存の強みを壊さない

## サイト構造

```
content/docs/
├── start/          # weight 10: P4Usとは（入口）
│   ├── how-to-use.md    # weight 11: 使い方（Pick upカード含む）
│   └── ai-start-pack.md # weight 12: AIスタートパック
├── essence/        # weight 30: リテラシー
│   ├── ai-partnership.md    # weight 33: AIとの付き合い方
│   ├── prompt-landscape.md  # weight 34: プロンプトの現在地
│   ├── external-tools.md    # weight 35: ツール連携
│   ├── learned-model.md     # weight 36: 学習済みモデル
│   ├── basic-prompt.md, markdown.md, mindset.md, risk-management.md, ai_bias.md
│   └── ...
├── basic/          # weight 40: 基本
├── intermediate/   # weight 50: 応用
├── cases/          # weight 60: プロンプト集
├── archive/        # weight 200: アーカイブ（過去講演、歴史的記録）
├── links.md        # weight 210: リンク集
└── support/        # FAQ
```

## Hugo テーマ・ショートコード

- テーマ: **Lotusdocs**
- アラート: `{{% alert icon="" context="success/warning/info/dark" %}}` ... `{{% /alert %}}`
- インラインアラート: `{{< alert context="info" text="..." />}}`
- テーブル: `{{< table "table-responsive" >}}` ... `{{< /table >}}`
- 内部リンク: `[テキスト]({{% relref "/docs/path/file.md" %}})`
- 日時テーブル: 各ページ冒頭に使用した生成AIとその日時を記載（モデルバージョン番号は含めない）

## 品質チェックリスト

改修後に以下を確認:

- [ ] `grep -r "作成中\|開発途中"` でマーカー残存なし
- [ ] `grep -r "GPT-3.5\|GPT-4"` でモデルバージョン残存なし（archive/と出力例内は除外）
- [ ] `grep -r "udify.app"` でDifyスクリプト残存なし
- [ ] 修正した404リンクのHTTPステータス確認
- [ ] lastmodは内容を実際に変更したファイルのみ更新
- [ ] archive/ 内は歴史的記録として基本的に据え置き

## 過去のPR履歴

- **PR #1** (Phase 1): `renovation-2026` - 12ファイル更新、最新化・普遍化・新規コンテンツ
- **PR #2** (Phase 2): `phase2-renovation-2026` - 22ファイル更新、機械的修正・モデル名普遍化・品質改善
- **PR #3** (Phase 3): `phase3-strategic-update-2026` - AIスタートパック新設、プロンプトの現在地新設、how-to-use/zero-shot-cot更新
