---
title: Wiki 全体サマリー
type: overview
updated: 2026-05-11
---

# AI 第二脳 — Wiki 全体サマリー

> hiroshi_takizawa の Obsidian_hub Wiki の現在の状態と全体像。

---

## このWikiについて

**目的**: Hiroshi Takizawa の知識・情報・ビジネスコンテキストを一元管理する AI 第二脳。  
**方式**: Karpathy の LLM Knowledge Base システム（RAGではなくWiki継続構築型）。  
**実装**: Claude Code（書き手） + Obsidian（可視化） + CLAUDE.md（スキーマ）。

---

## 現在の知識の状態（2026-05-11）

### カバーされているテーマ
- **LLM型知識管理**: RAGとの違い、3レイヤー構造、Ingest/Query/Lint操作
- **ツール理解**: Claude Code、Obsidian、agent-browser の役割と連携
- **第二脳の設計**: Vault構造、outputs/ 運用、index/log管理
- **実践運用**: 月次ヘルスチェック、エラー複利リスクの回避

### まだカバーされていないテーマ（今後 Ingest 予定）
- hiroshi_takizawa のビジネス情報（Claude Master Folder → Ingest推奨）
- 進行中プロジェクト（seo-managed-agents ダッシュボードなど）
- 個人的な目標・好み・作業スタイル

---

## ソース数・ページ数

| カテゴリ | 数 |
|---------|---|
| Raw Sources | 3 |
| Entity ページ | 4 |
| Concept ページ | 4 |
| Source 要約 | 3 |
| **合計 Wiki ページ** | **11** |

---

## 次に取り込むべきソース（推奨順）

1. `Claude Master Folder/Instructions.md` — Hiroshi の作業ルール・好み
2. `Claude Master Folder/Memory.md` — 蓄積された記憶
3. `Claude Master Folder/Context.md` — プロジェクトコンテキスト
4. `seo-managed-agents/CLAUDE.md` — 技術プロジェクトの文脈

---

## このWikiの使い方

```
質問する     → 「〜について教えて」「〜と〜の違いは」
取り込む     → 「raw/ に [X] を追加したので ingest して」
lint する    → 「wiki を lint して」
俯瞰する     → この overview.md と index.md を読む
```
