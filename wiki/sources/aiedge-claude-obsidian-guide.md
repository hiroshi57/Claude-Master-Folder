---
title: Claude Code + Obsidian Ultimate Guide — aiedge 記事 要約
type: source
tags: [Claude Code, Obsidian, 第二脳, セットアップ, 実践]
sources: [aiedge-claude-obsidian-guide.md]
updated: 2026-05-07
---

# Claude Code + Obsidian Ultimate Guide — aiedge 記事 要約

> **原典**: aiedge.co / @aiedge_  
> **著者**: aiedge  
> **インスピレーション**: Karpathy の LLM Knowledge Base ツイート

---

## 主要メッセージ

**Claude Code + Obsidian は「毎回コンテキストを再入力する問題」を根本から解決する。**  
自分の全データに AI がアクセスできる状態を作ることで、精度の高いアウトプットが生まれる。

---

## 要点（5つ）

1. **5分セットアップ**: Obsidian DL → Vault 作成 → Claude Code で Vault を開く → CLAUDE.md 入力 → データ追加
2. **Chrome Extension**: Obsidian Web Clipper でウェブ記事を raw/ に即保存
3. **2 Vault 構成**: ビジネス用・個人用を分ける（Karpathy 推奨）
4. **メガプロンプト生成**: 自分のデータ全体を使ってカスタマイズされたプロンプトを自動生成
5. **Orphans 活用**: リンクのないアイデアを「弱点」として可視化・強化

---

## 実践的なユースケース

- **プロンプト精度向上**: ビジネス計画・執筆コンテキストへのアクセスでメガプロンプト生成
- **ナレッジ統合**: YouTube 動画、記事、ノートを一元管理
- **アイデアリンク**: 自動的にアイデア間の繋がりが形成される
- **メンタル帯域の解放**: 記憶・整理・接続を AI に委ねて本質業務に集中

---

## セットアップで重要な点

- **CLAUDE.md が要**: Karpathy のシステムプロンプトを貼り付けることで AI が「Wiki 管理者」モードになる
- **Obsidian を触らなくてもよい**: Claude Code が md ファイルを書けば Obsidian に自動反映される
- **初期データが必要**: 空のまま使っても機能しない。既存ノートアプリからエクスポートして入力

---

## hiroshi_takizawa への関連性

このガイドの手順は `Obsidian_hub/` として実装済み:
- セットアップ手順: ✅ 完了
- 初期データ Ingest: → 進行中（このセッション）

---

## 関連ページ
- [[concepts/llm-knowledge-base]]
- [[concepts/obsidian-vault-structure]]
- [[entities/obsidian]]
- [[entities/claude-code]]
- [[sources/karpathy-llm-knowledge-base]]
