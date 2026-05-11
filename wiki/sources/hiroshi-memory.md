---
title: Hiroshi Memory — 蓄積された作業記憶・決定事項
type: source
tags: [個人コンテキスト, 好み, プロジェクト, 決定事項]
sources: [hiroshi-memory.md]
updated: 2026-05-11
---

# Hiroshi Memory — 蓄積された作業記憶・決定事項

## 概要
Hiroshi Takizawa（瀧澤 浩）の Claude との作業履歴から蓄積された記憶ファイル。
好み・訂正・重要な決定事項・進行中プロジェクトを記録。

---

## Preferences（好み）

- **出力スタイル**: 簡潔・箇条書き優先（長文の前置き不要）
- **言語**: 日本語（コードコメントも日本語可）
- **セキュリティ**: `.env`（APIキー）は絶対に公開リポジトリに含めない
- **リポジトリ方針**: 個人設定ファイルと公開コードは別管理

---

## Corrections（やめてほしいこと）

- 曖昧な日本語指示ではなく具体的なCLIコマンドを使う
- 個人設定ファイルと公開リポジトリを同じgit管理にしない

---

## 重要な決定事項

| 日付 | 決定内容 |
|------|---------|
| 2026-05-07 | Karpathy方式のAI第二脳を構築（ツール: OpenKB + Obsidian） |
| 2026-05-07 | リポジトリ: hiroshi57/Claude-Master-Folder（Public） |
| 2026-05-07 | 認証: GitHub Actions WIF（APIキー不要） |
| 2026-05-07 | ローカル実行時は `.env` に `LLM_API_KEY` を記入 |

---

## 進行中プロジェクト（2026-05-07 時点）

### AI 第二脳（Obsidian_hub）
- [x] Obsidian_hub セットアップ（raw/ wiki/ CLAUDE.md）
- [x] GitHub Actions WIF ワークフロー作成
- [ ] Anthropic Console WIF 設定（Service Account / Issuer / Rule）
- [ ] GitHub Secrets に WIF 変数を登録

### AI-info-dashboard
- [x] ハーネス設計ページ追加（2026-05-07）

### seo-managed-agents ダッシュボード
- [x] ダッシュボード大規模改修（2026-05-07）
- [x] GA4 / Search Console 実API接続
- [ ] ChatGPT / Gemini 実LLMO調査

---

## Personal Context

- **環境**: Windows 11、Claude Code、VS Code、Git Bash
- **GitHub**: hiroshi57
- **メール**: takizawa.hiroshi@digitalidentity.co.jp

---

## 関連ページ
- [[concepts/llm-knowledge-base]]
- [[entities/andrej-karpathy]]
