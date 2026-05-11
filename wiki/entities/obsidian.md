---
title: Obsidian
type: entity
tags: [ツール, ノートアプリ, マークダウン, PKM]
sources: [aiedge-claude-obsidian-guide.md, karpathy-llm-knowledge-base.md]
updated: 2026-05-07
---

# Obsidian

## 概要
ローカルファイルベースのマークダウンノートアプリ。  
データは端末上の markdown ファイル（.md）として保存されるため、Claude Code から直接読み書き可能。

## このシステムでの役割
- Vault = Claude Code がアクセスするフォルダ
- Wiki の可視化（グラフビュー、バックリンク）
- ユーザーが Obsidian で読む ← Claude が Wiki を書く

## 主要機能（AIシステムとの連携で特に有用）

| 機能 | 用途 |
|------|------|
| Graph View | Wiki ページの接続関係を可視化 |
| Orphans 表示 | リンクのない孤立ページを検出 |
| Chrome Extension | ウェブ記事を raw/ に直接保存 |
| Dataview プラグイン | frontmatter を使った動的テーブル |
| Marp プラグイン | Wiki からスライド生成 |

## 設定推奨
- 添付ファイルパス: `raw/assets/`（Obsidian Settings → Files and links）
- 「Download attachments for current file」ショートカット: Ctrl+Shift+D

## 入手先
https://obsidian.md/

## 関連ページ
- [[concepts/llm-knowledge-base]]
- [[entities/claude-code]]
- [[concepts/obsidian-vault-structure]]
