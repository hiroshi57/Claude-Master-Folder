---
title: LLM Knowledge Base（LLM 型知識ベース）
type: concept
tags: [AI, 知識管理, Wiki, 第二脳, Karpathy]
sources: [karpathy-llm-knowledge-base.md, aiedge-claude-obsidian-guide.md]
updated: 2026-05-07
---

# LLM Knowledge Base（LLM 型知識ベース）

## 一言で言うと
LLM が毎回ゼロから検索するのではなく、**時間とともに成長する Wiki を構築・維持する**システム。

## RAG との違い

| 方式 | 仕組み | 問題点 |
|------|--------|--------|
| **RAG** | 質問ごとにドキュメントを検索して回答 | 知識が蓄積されない。毎回再発見が必要 |
| **LLM Knowledge Base** | LLM が Wiki を構築・更新し続ける | ✅ 知識が複利で蓄積される |

> *"The wiki is a persistent, compounding artifact."* — Karpathy

## 3レイヤー構造

```
Raw Sources（ソース）         → 読み取り専用・変更禁止
        ↓ Ingest
Wiki（構造化知識）            → LLM が管理・更新
        ↓ Query
Answer（回答）                → 価値ある回答はWikiに保存される
```

### Layer 1: Raw Sources
- ユーザーが追加・管理する「事実のソース」
- 記事、論文、ノート、CSV、PDF テキスト
- **LLM は絶対に変更しない**

### Layer 2: Wiki
- LLM が作成・更新する markdown ページ群
- エンティティページ、概念ページ、ソース要約、比較分析
- ユーザーは読む側、LLM は書く側

### Layer 3: Schema
- `CLAUDE.md` または `AGENTS.md`
- LLM に Wiki の構造・規約・ワークフローを伝える設定ファイル
- ユーザーと LLM が共同で進化させる

## 3つの操作

### Ingest（取り込み）
新ソース → LLM が読む → Wiki ページ作成・更新 → index.md / log.md 更新  
1ソースで 10〜15 ページが更新されることもある

### Query（質問）
index.md → 関連ページ特定 → 引用付き回答 → 価値ある回答はWikiに保存

### Lint（健全性チェック）
矛盾検出 / 古いクレーム更新 / 孤立ページ検出 / 欠落概念の発見

## なぜ強力なのか

1. **知識の複利効果** — 新しいソースが既存知識を強化・補完する
2. **コンテキストの永続性** — 新しい AI ツールに移行しても知識が失われない
3. **接続の可視化** — アイデア間のリンクが自動形成される
4. **毎回コンテキスト入力不要** — スキーマで LLM が自分で文脈を把握する

## 実装ツール
- Claude Code + Obsidian（hiroshi_takizawa の採用構成）
- qmd（大規模時の検索エンジン：BM25/ベクトル検索 + LLM リランク）

## 関連ページ
- [[concepts/rag-vs-wiki]]
- [[concepts/obsidian-vault-structure]]
- [[entities/andrej-karpathy]]
- [[entities/claude-code]]
- [[entities/obsidian]]
