---
title: RAG vs LLM Wiki — 知識管理方式の比較
type: concept
tags: [RAG, Wiki, AI, 知識管理, 比較]
sources: [karpathy-llm-knowledge-base.md]
updated: 2026-05-07
---

# RAG vs LLM Wiki — 知識管理方式の比較

## 比較表

| 項目 | RAG | LLM Wiki（Karpathy方式） |
|------|-----|--------------------------|
| **仕組み** | 質問時にドキュメントを検索 | 事前に Wiki を構築・更新 |
| **知識の蓄積** | なし（毎回ゼロから） | あり（複利で成長） |
| **複雑な質問** | 5ドキュメント横断が難しい | Wiki 内で既に統合済み |
| **代表例** | NotebookLM, ChatGPT file upload | Karpathy's system, Obsidian_hub |
| **セットアップコスト** | 低 | 中 |
| **長期的な価値** | 低（知識が残らない） | 高（知識が積み上がる） |

## RAG の問題点

> *"The LLM is rediscovering knowledge from scratch on every question. There's no accumulation."* — Karpathy

- 毎回同じ文脈を再検索・再解釈する非効率
- 5つのドキュメントにまたがる微妙な質問に弱い
- 会話が終わると知識がリセットされる

## LLM Wiki が解決すること

- **一度コンパイルされた知識**が永続する
- 新しいソースは既存 Wiki に**統合**される（追加ではなく）
- 矛盾を検出・更新できる（Lint）
- 回答自体が Wiki ページになり、さらに積み上がる

## いつ RAG を使うか

- 大量ドキュメント（数千件以上）のリアルタイム検索
- 最新情報が頻繁に変わる場合
- 構造化が難しい非定型データ

## いつ LLM Wiki を使うか

- 個人の知識ベース・第二脳の構築
- ビジネス戦略・研究テーマの体系化
- 数ヶ月〜数年にわたる継続的な知識蓄積

## 関連ページ
- [[concepts/llm-knowledge-base]]
- [[entities/andrej-karpathy]]
