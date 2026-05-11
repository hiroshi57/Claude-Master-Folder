---
name: GitHub security cleanup (2026-05-07)
description: Full audit and cleanup of all 69 GitHub repos (21 public + 48 private) for sensitive data leakage
type: project
---

2026-05-07 に公開21件・プライベート48件、計69リポジトリの全件セキュリティ監査と自動クリーンアップを実施した。

**Why:** 個人情報・バイオメトリクスデータ・パスワードハッシュ・ローカルパスなどが公開リポジトリに含まれていたため。

**修正したリポジトリ（8件）:**
- `face-auth` — face_auth.db（顔特徴量）・logs/face_auth.log（実名「滝沢浩司」+顔認証スコア）を git filter-repo で履歴ごと削除
- `making-to-a-comp` — data/credentials.json（パスワードハッシュ）・company/employees.json（銀行情報）を履歴削除、auth.py のハードコード JWT secret を削除
- `fishing-area` — logs/ を履歴削除
- `neo-di-marketing` — .claude/settings.local.json（ローカルパス）を履歴削除
- `project-hub` — .env を履歴削除
- `di-kb` — .claude/state/, sessions/, settings.local.json を履歴削除
- `security-app` — settings.json, settings.local.json（ローカルパス）を履歴削除
- `persona-genie-new` — .claude/settings.local.json を履歴削除

**全リポジトリに追加した .gitignore ルール:**
`logs/`, `*.db`, `*.sqlite`, `.env`, `.claude/settings.local.json`, `.claude/state/`, `.claude/sessions/`

**プライベート48件スキャン結果:** APIキーハードコードなし、追加の漏洩なし（クリーン）

**How to apply:** 今後 Claude Code のセッション状態ファイル（.claude/state/, settings.local.json）はコミットしないよう .gitignore で恒久除外済み。新リポジトリ作成時も同ルールを適用すること。
