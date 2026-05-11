# Lint レポート — 2026-05-11

> 操作: lint | 対象: wiki/ 全ページ（13ページ）| 実行者: Claude Code

---

## ✅ 問題なし

| チェック項目 | 結果 |
|------------|------|
| ページ間の矛盾 | なし |
| 孤立ページ（リンクなし） | なし |
| ソース未裏付けのクレーム | なし |

---

## 🔧 修正済み

### andrej-karpathy.md — 引用の重複削除
- **問題**: *"Instead of just retrieving..."* の引用が「主な貢献」と「主な発言・引用」の2箇所に存在
- **対応**: 「主な貢献」セクションから重複を削除
- **commit**: `fix: andrej-karpathy.md の引用重複を削除（lint修正）`

---

## 📝 推奨アクション（未対応）

| 優先度 | アクション |
|--------|-----------|
| 🔴 高 | `Instructions.md` の `[記入してください]` を埋めて ingest |
| 🟡 中 | `concepts/wif-github-actions.md` を新規作成（Memory に未完了タスクあり） |
| 🟡 中 | `concepts/outputs-workflow.md` を新規作成（各所に分散している説明を統合） |
| 🟢 低 | Memory.md に 2026-05-11 の作業を追記して再 ingest |

---

## 📊 現在の wiki 状態

| カテゴリ | 数 |
|---------|---|
| Raw Sources | 4 |
| Entity ページ | 5 |
| Concept ページ | 4 |
| Source 要約 | 4 |
| **合計 Wiki ページ** | **13** |

---

*次回 lint 推奨: 2026-06-11（月次）*
