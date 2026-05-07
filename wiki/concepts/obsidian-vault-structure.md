---
title: Obsidian Vault 構造 — AI 第二脳の設計
type: concept
tags: [Obsidian, Vault, フォルダ構造, 設計, 第二脳]
sources: [aiedge-claude-obsidian-guide.md, karpathy-llm-knowledge-base.md]
updated: 2026-05-07
---

# Obsidian Vault 構造 — AI 第二脳の設計

## 推奨フォルダ構造

```
Obsidian_hub/                   ← Claude Code がアクセスするルート
├── CLAUDE.md                   ← スキーマ（LLMへの指示書）
├── raw/                        ← ソース（読み取り専用・変更禁止）
│   ├── assets/                 ← 画像・添付ファイル
│   └── [ソースファイル群.md]
└── wiki/                       ← Claude が管理する構造化知識
    ├── index.md                ← 全ページカタログ（自動更新）
    ├── log.md                  ← 操作ログ（追記のみ）
    ├── overview.md             ← 全体サマリー
    ├── entities/               ← 人物・組織・ツール
    ├── concepts/               ← 概念・トピック
    └── sources/                ← ソース要約ページ
```

## 各フォルダの役割

### raw/
- **ユーザーが管理**（Claude は読むだけ）
- Obsidian Chrome Extension でウェブ記事を直接保存
- データを追加したら Claude に「ingest して」と伝える

### wiki/
- **Claude が管理**（ユーザーは読むだけ）
- Ingest → 自動的にページが生成・更新される

## 2 Vault 構成（Karpathy 推奨）

| Vault | 用途 |
|-------|------|
| ビジネス Vault | 仕事・プロジェクト・戦略 |
| 個人 Vault | 目標・アイデア・学習 |

## index.md と log.md の違い

| ファイル | 目的 | 更新タイミング |
|---------|------|--------------|
| `index.md` | コンテンツカタログ（何があるか） | 毎 Ingest 時 |
| `log.md` | 時系列ログ（何をしたか） | 追記のみ |

## 画像管理の設定

Obsidian Settings → Files and links:
- `Attachment folder path` → `raw/assets/`
- ホットキー設定: 「Download attachments for current file」→ `Ctrl+Shift+D`

## 関連ページ
- [[concepts/llm-knowledge-base]]
- [[entities/obsidian]]
- [[entities/claude-code]]
