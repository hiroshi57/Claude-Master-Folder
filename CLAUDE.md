# CLAUDE.md — AI Second Brain Schema
> Karpathy LLM Knowledge Base システム（hiroshi_takizawa 版）
> このファイルは Claude Code がこの Vault をどう操作するかを定義するスキーマ。

---

## システム概要（The Core Idea）

このシステムは通常の RAG（検索→回答）とは異なる。  
RAG は毎回ゼロからドキュメントを検索するが、このシステムは**Wiki を継続的に構築・更新**する。

```
Raw Sources（ソース）  →  Wiki（構造化知識）  →  Query（質問・活用）
   [読み取り専用]          [Claude が管理]         [答えが蓄積される]
```

知識は一度コンパイルされ、新しいソースが来るたびに更新される。  
これが「第二脳」が時間とともに賢くなる理由。

---

## フォルダ構造

```
Obsidian_hub/
├── CLAUDE.md              ← このファイル（スキーマ）
├── raw/                   ← ソースドキュメント（読み取り専用・変更禁止）
│   ├── assets/            ← 画像・添付ファイル
│   └── [ソースファイル群]
├── wiki/                  ← Claude が管理する構造化 Wiki
│   ├── index.md           ← 全ページのカタログ（自動更新）
│   ├── log.md             ← 操作ログ（追記のみ）
│   ├── overview.md        ← 全体サマリー
│   ├── entities/          ← 人物・組織・ツールのページ
│   ├── concepts/          ← 概念・トピックのページ
│   └── sources/           ← ソース要約ページ
└── ようこそ.md
```

---

## 3つのレイヤー

### Layer 1: Raw Sources（raw/）
- **読み取り専用** — Claude は絶対に変更しない
- 記事、ノート、CSV、PDF テキスト、トランスクリプトなど
- ユーザーが追加・管理する「事実のソース」

### Layer 2: Wiki（wiki/）
- **Claude が完全に管理する**
- ソースを読み込み、エンティティページ・概念ページ・要約を作成
- 新しいソースが来たら既存ページを更新・リンク追加
- ユーザーは読む側、Claude は書く側

### Layer 3: Schema（このファイル）
- Claude に Wiki の構造・規約・ワークフローを伝える
- ユーザーと Claude が共同で進化させる
- **セッション開始時に必ず読む**

---

## 操作ワークフロー

### Ingest（新しいソースを取り込む）

ユーザーが `raw/` にファイルを追加して「取り込んで」と言ったとき：

1. ソースを読み込む
2. 主要なポイントをユーザーと確認
3. `wiki/sources/` に要約ページを作成
4. 関連する `wiki/entities/` `wiki/concepts/` ページを更新
5. `wiki/index.md` を更新
6. `wiki/log.md` に記録を追記

**1ソースで 10〜15 ページが更新されることもある。**

### Query（質問する）

ユーザーが Wiki に質問したとき：

1. `wiki/index.md` を読んで関連ページを特定
2. 関連ページを読み込む
3. 引用付きで回答
4. 価値ある回答は Wiki の新しいページとして保存

### Lint（Wiki の健全性チェック）

定期的に実行（ユーザーが「lint して」と言ったとき）：

- ページ間の矛盾を検出
- 古くなったクレームを更新
- リンクのないページ（孤立ページ）を検出
- 重要な概念でページがないものをリストアップ
- 新しい調査テーマを提案

---

## ファイル規約

### index.md の形式

```markdown
# Wiki Index
## Entities（人物・組織・ツール）
- [[entities/Claude]] — Anthropic の AI アシスタント（2ソース）
## Concepts（概念・トピック）
- [[concepts/LLM-Knowledge-Base]] — Karpathy 提唱の Wiki 型記憶システム
## Sources（ソース要約）
- [[sources/aiedge-memory-guide]] — Claude メモリシステム完全ガイド
```

### log.md の形式

```markdown
## [2026-05-07] ingest | Claude メモリシステム記事
概要: 3層メモリシステムの解説記事を取り込み。
更新ページ: entities/Claude, concepts/LLM-Knowledge-Base, sources/aiedge-memory-guide
```

### Wiki ページの frontmatter

```yaml
---
title: ページタイトル
type: entity | concept | source | query-result
tags: [タグ1, タグ2]
sources: [ソースファイル名]
updated: 2026-05-07
---
```

---

## 日本語設定

- **すべての Wiki ページは日本語で記述する**
- ファイル名は英語スラッグ（例: `concepts/llm-knowledge-base.md`）
- ページタイトル・本文は日本語
- frontmatter の値は英語可

---

## 初期データとして優先取り込むもの

1. `Claude Master Folder/Instructions.md` — ユーザールール・好み
2. `Claude Master Folder/Memory.md` — 蓄積された記憶
3. `Claude Master Folder/Context.md` — プロジェクトコンテキスト
4. `your_comp_hub/CLAUDE.md` — 技術制約・開発ルール
5. 追加データ（ユーザーが指定）

---

## セッション開始時の定型手順

```
1. このファイル（CLAUDE.md）を読む
2. wiki/index.md を読んで現在の Wiki 状態を把握
3. wiki/log.md の最新エントリを確認
4. ユーザーのタスクに着手
```

---

*スキーマバージョン: 1.0 | 作成: 2026-05-07*
