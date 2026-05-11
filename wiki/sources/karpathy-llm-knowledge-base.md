---
title: LLM Knowledge Bases — Karpathy Gist 要約
type: source
tags: [Karpathy, LLM, Wiki, 知識管理, 第二脳]
sources: [karpathy-llm-knowledge-base.md]
updated: 2026-05-07
---

# LLM Knowledge Bases — Karpathy Gist 要約

> **原典**: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f  
> **著者**: Andrej Karpathy  
> **バイラル**: 2026年4月3日頃（X/Twitter）

---

## 主要メッセージ

**RAG は知識を蓄積しない。LLM が Wiki を構築・維持する方式こそが真の知識ベース。**

「*The wiki is a persistent, compounding artifact.*」

---

## 要点（5つ）

1. **RAG の限界**: 毎回ゼロから検索・解釈するため知識が積み上がらない
2. **3レイヤー構造**: Raw Sources → Wiki → Schema の明確な責任分担
3. **Ingest ワークフロー**: 1ソースで 10〜15 Wiki ページが更新される
4. **Query のフィードバックループ**: 良い回答自体がWikiページになる
5. **Lint**: 定期的な健全性チェックで Wiki の品質を維持する

---

## 実装のポイント

- **Schema（CLAUDE.md）**が最重要 — LLM を「汎用チャットボット」から「規律ある Wiki 管理者」に変える
- **index.md** と **log.md** の2ファイルが Wiki のナビゲーションを支える
- スケールしたら `qmd`（ハイブリッド BM25/ベクトル検索）の導入を検討

---

## このシステムへの適用

hiroshi_takizawa の `Obsidian_hub/` は本 Gist の設計を直接実装している:
- `raw/` → Raw Sources（読み取り専用）
- `wiki/` → LLM-managed Wiki
- `CLAUDE.md` → Schema

---

## 関連ページ
- [[concepts/llm-knowledge-base]]
- [[concepts/rag-vs-wiki]]
- [[entities/andrej-karpathy]]
