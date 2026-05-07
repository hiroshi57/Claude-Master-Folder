---
title: Claude Code
type: entity
tags: [ツール, Anthropic, AI, CLI]
sources: [aiedge-claude-obsidian-guide.md]
updated: 2026-05-07
---

# Claude Code

## 概要
Anthropic が提供する CLI / デスクトップ AI アシスタント。  
ファイルシステムへの直接アクセスを持ち、コードの読み書き・実行が可能。

## このシステムでの役割
- Wiki の **唯一の書き手**（raw/ は読み取り専用）
- ソース Ingest → Wiki ページ生成・更新
- ユーザーの質問に Wiki を参照して回答
- Lint（Wiki 健全性チェック）の実行

## Obsidian との連携
1. Obsidian Vault フォルダを Claude Code に選択して開く
2. CLAUDE.md スキーマを読み込ませる
3. あとは「[X] を取り込んで」「〜について教えて」と話しかけるだけ

## ポイント
- Obsidian の UI を一切使わなくてもシステムは動作する
- Claude Code が md ファイルを更新すると Obsidian の画面にリアルタイム反映される

## 関連ページ
- [[concepts/llm-knowledge-base]]
- [[entities/obsidian]]
- [[entities/andrej-karpathy]]
