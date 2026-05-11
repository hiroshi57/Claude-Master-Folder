# Claude Code + Obsidian Ultimate Guide — AI Second Brain

> ソース: aiedge.co / @aiedge_ (Instagram/X)  
> 著者: aiedge  
> 取得日: 2026-05-07

---

## 概要

Claude Code + Obsidian を組み合わせた AI 第二脳システムのガイド。  
Andrej Karpathy の LLM Knowledge Base ツイートからインスピレーションを得た実践的な構築方法。

---

## システムの4要素

1. **Your data** — 記事、ノート、トランスクリプト、アイデアなど
2. **Organization** — Claude Code による Obsidian 内の整理
3. **Instant Prompting** — データベースにいつでも質問できる
4. **Evolving Memory** — 時間とともに賢くなる記憶能力

---

## セットアップ手順（5分）

### Step 1: Obsidian ダウンロード
https://obsidian.md/

### Step 2: Vault のセットアップ
- Obsidian を開き「Vault」を作成（= Claude Code がアクセスできるフォルダ）
- Vault は markdown ファイルを保存するデスクトップフォルダ

### Step 3: Claude Code のセットアップ
- デスクトップアプリを使う
- メインチャットボックスで「Select Folder」→ Obsidian Vault を選択

### Step 4: システムプロンプト入力
Karpathy のシステムプロンプト（CLAUDE.md スキーマ）をメインチャットボックスに貼り付け

### Step 5: データベース構築
- 既存ノートアプリからデータをエクスポート（Notion は CSV）
- 記事・ブックマーク・アイデアを入力
- Claude Code に「[X] を取り込んで」と伝えると Wiki に統合される

---

## Pro Tips

### 1. Obsidian Chrome Extension
- Chrome の拡張機能でウェブ記事を markdown に変換
- 「add to Obsidian」ボタンでデータをワンクリック追加
- 追加後に Claude Code に「ingest して」と伝えると Wiki に統合

### 2. Vault を分ける
- ビジネス/仕事用 Vault
- 個人/目標用 Vault  
（Karpathy 推奨の構成）

### 3. 実用的な使い方
- 最も効果的なユースケース：LLM プロンプトの精度向上
- 自分のビジネス計画・執筆コンテキスト・過去のデータへのアクセスで
  カスタマイズされたメガプロンプトを生成

### 4. Orphans（孤立ページ）の活用
- Obsidian の Orphans 機能でリンクのないデータポイントを可視化
- 「弱点」= まだ繋がっていないアイデアの発見に使う
- 右上3点メニューで切り替え可能

---

## このシステムのメリット

- 毎回コンテキストを再入力する必要がない
- 新しい AI ツールに移行しても知識が持続する
- アイデアが互いにリンクされ、繋がりが見える
- Claude が全ライフデータにアクセスして精度の高い出力を生成

---

## 潜在的なデメリット

1. **視覚化が苦手な人には向かない** — データの可視化が主要メリットのため
2. **メンテナンスが必要** — データ入力なしでは機能しない
3. **ストレージ消費** — markdown ファイルがデバイスに蓄積される

---

## 関連リソース

- Karpathy LLM Knowledge Base Gist: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
- Obsidian: https://obsidian.md/
- チートシート: https://www.aiedgehq.co/
