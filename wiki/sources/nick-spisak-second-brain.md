---
title: Nick Spisak — How to Build Your Second Brain
type: source
tags: [第二脳, 実践ガイド, agent-browser, ヘルスチェック, Karpathy]
sources: [nick-spisak-second-brain.md]
updated: 2026-05-11
---

# Nick Spisak — How to Build Your Second Brain

## 概要
@NickSpisak_ による Karpathy LLM Knowledge Base の実践的な 8 ステップ実装ガイド。
Karpathy が示した設計原則を「今日から始められる手順」に落とし込み、
`agent-browser` による自動収集と月次ヘルスチェックを加えた実用版。

---

## 8 ステップ要約

### Step 1: 3 つのフォルダを作る（2分）
```
my-knowledge-base/
  raw/      ← ソース素材（AI が整理する）
  wiki/     ← AI が構造化する場所
  outputs/  ← AI が生成した回答・レポート
```
アプリ不要。アカウント不要。フォルダ 3 つだけ。

### Step 2: raw/ を埋める（10分）
- 記事・ノート・スクショ・議事録・論文・ブックマーク — とにかく全部
- 整理しない。リネームしない。クリーンにしない。**それは AI の仕事**
- Nick は 17 個の raw ファイルを X コンテンツパイプラインで運用中

### Step 3: agent-browser で収集を自動化（任意）
→ [[concepts/agent-browser]] 参照

### Step 4: Schema ファイル（CLAUDE.md）を書く（5分）
- `CLAUDE.md` または `AGENTS.md` または `README.md`（名前は問わない）
- Karpathy: *"super simple and flat"* — DB 不要、プラグイン不要、テキストだけ
- AI への指示書。プロジェクトごとの CLAUDE.md と同じ概念

### Step 5: AI に Wiki を構築させる（15分）
```
"Read everything in raw/. Then compile a wiki in wiki/ 
following the rules in CLAUDE.md..."
```
- 完成すると wiki/ にトピック別 .md が揃い、INDEX.md で検索可能になる
- **wiki は手で編集しない**。読む専用、書くのは AI

### Step 6: 質問して答えを保存する（継続）
- 「wiki/ の内容から、自分の理解のギャップを 3 つ挙げて」
- 「Source A と Source B の [概念] に関する見解の違いは？」
- **答えは outputs/ に保存、または wiki に反映** → 質問するたびに賢くなる

### Step 7: 月次ヘルスチェック（重要）
```
"wiki/ 全体をレビューして。矛盾を検出、説明のないトピックを発見、
ソースに裏付けのないクレームを列挙、欠落している記事を 3 件提案して"
```
> **@HFloyd の警告**: *"outputs を保存すると、エラーも複利になる"*
> 誤った内容が wiki に保存されると次の回答がその誤りの上に構築される。
> 月次チェックで修正しなければエラーが雪だるま式に蓄積する。

### Step 8: Obsidian は必須ではない
- Karpathy: *"ただのネストした .md ファイル群"*
- Claude Code / VS Code / Obsidian / Notepad — AI はどれでもよい
- **重要なのはフォルダ構造とスキーマ** — ツールではない
- Obsidian に 47 プラグインは「Notion トラップ」と同じ

---

## キーインサイト

| インサイト | 出典 |
|-----------|------|
| 3 フォルダ構造（raw / wiki / outputs） | Nick Spisak |
| agent-browser で raw/ を自動充填 | Nick Spisak |
| エラーの複利リスク → 月次ヘルスチェック | @HFloyd (via Nick) |
| "super simple and flat" が最強 | Karpathy (Nick 引用) |

---

## 関連ページ
- [[concepts/llm-knowledge-base]]
- [[concepts/agent-browser]]
- [[entities/nick-spisak]]
- [[entities/andrej-karpathy]]
- [[sources/karpathy-llm-knowledge-base]]
