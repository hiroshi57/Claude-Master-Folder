---
title: agent-browser — AI エージェント用ブラウザ CLI
type: concept
tags: [CLI, ウェブスクレイピング, 自動化, Vercel Labs, raw収集]
sources: [nick-spisak-second-brain.md]
updated: 2026-05-11
---

# agent-browser — AI エージェント用ブラウザ CLI

## 概要
Vercel Labs が開発した無料の CLI ツール。  
AI エージェントがリアルブラウザを操作し、ウェブページのテキストを抽出して `raw/` フォルダに保存できる。  
GitHub Stars: 26K+（2026年5月時点）

## インストール

```bash
npm install -g agent-browser
agent-browser install   # 専用 Chrome をダウンロード
```

## 基本的な使い方

```bash
# ページを開く
agent-browser open https://some-article-you-want.com

# テキストを取得
agent-browser get text "article"
```

取得したテキストを `raw/` のファイルにパイプするだけで、手動コピペ不要で raw/ が充填される。

## 強み

| 項目 | 内容 |
|------|------|
| **JS ヘビーサイト対応** | 動的コンテンツのロードが必要なページも取得可能 |
| **ログイン済みページ** | 認証が必要なページも対応 |
| **インタラクション** | スクロール、「もっと読む」クリック、メニュー操作 |
| **トークン効率** | Playwright MCP 比 **82% 削減** → 同じセッションで 5〜6 倍多くのページを処理 |

## LLM Knowledge Base での活用フロー

```
1. 取り込みたい記事 URL を見つける
2. Claude Code に「この URL をスクレイピングして raw/ に保存して」と伝える
3. agent-browser が自動でページを開き、テキストを抽出、ファイル保存
4. raw/ が自動充填される → 「ingest して」で wiki が更新される
```

## Playwright MCP との比較

| ツール | トークン消費 | 用途 |
|--------|-------------|------|
| Playwright MCP | 高い | 複雑なブラウザ自動化 |
| **agent-browser** | **82% 少ない** | **知識収集・テキスト抽出** |

## 注意点
- Windows（Git Bash / mingw64）環境では動作検証が必要
- WSL または macOS/Linux での使用が推奨される場合がある

## 関連ページ
- [[concepts/llm-knowledge-base]]
- [[entities/nick-spisak]]
- [[sources/nick-spisak-second-brain]]
