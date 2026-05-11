---
title: Andrej Karpathy
type: entity
tags: [AI研究者, OpenAI, Tesla, LLM]
sources: [karpathy-llm-knowledge-base.md, nick-spisak-second-brain.md]
updated: 2026-05-11
---

# Andrej Karpathy

## 概要
AI 研究者・エンジニア。元 OpenAI / Tesla の AI 責任者。  
LLM・深層学習の分野で世界的に著名。教育的なコンテンツでも知られる。

## 主な貢献（このシステムとの関連）

### LLM Knowledge Base システムの提唱
2026年4月3日頃にバイラルツイートで発表。  
RAG（検索型）ではなく、**LLMが継続的にWikiを構築・更新する**アプローチを提案。

> *"Instead of just retrieving from raw documents at query time, the LLM incrementally builds and maintains a persistent wiki."*

### 3レイヤー構造の提案
- Raw Sources（読み取り専用ソース）
- Wiki（LLMが管理する構造化知識）
- Schema（CLAUDE.md / AGENTS.md）

## 主な発言・引用

> *"Instead of just retrieving from raw documents at query time, the LLM incrementally builds and maintains a persistent wiki."*

> *"I'm trying to keep it super simple and flat. It's just a nested directory of .md files."*  
> — Nick Spisak 記事での引用（セットアップの複雑さについて）

## 関連リソース
- Gist: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
- Twitter: @karpathy

## 関連ページ
- [[concepts/llm-knowledge-base]]
- [[concepts/rag-vs-wiki]]
- [[sources/karpathy-llm-knowledge-base]]
