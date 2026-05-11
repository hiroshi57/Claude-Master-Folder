# Memory.md
> Claudeの自動更新メモリファイル。会話を通じて継続的に蓄積される。
> **Claude へ**: ユーザーの好み・訂正・パターンが判明したら、このファイルを自動更新すること。

---

## Preferences（好み）

- **出力スタイル**: 簡潔・箇条書き優先（長文の前置き不要）
- **言語**: 日本語（コードコメントも日本語可）
- **セキュリティ**: .env（APIキー）は絶対に公開リポジトリに含めない
- **リポジトリ方針**: 個人設定ファイル（Instructions/Memory/Context）と公開コードは別管理

---

## Corrections（訂正・やめてほしいこと）

- 「ingest して」など曖昧な日本語指示ではなく、具体的なCLIコマンドを使う（`openkb add <file>` 等）
- 個人設定ファイルと公開リポジトリを同じgit管理にしない

---

## Patterns（繰り返すパターン・作業スタイル）

- セッション開始時: `git status -sb` + `cat Plans.md` / NEXT_TASKS.md を確認
- 公開リポジトリ（GitHub Public）には個人情報・APIキーを含めない
- Claude-Master-Folder はローカル専用（git 管理しない）
- Obsidian_hub は GitHub で管理（hiroshi57/Claude-Master-Folder リポジトリ）

---

## Decisions（重要な決定事項）

- **2026-05-07**: Karpathy方式のAI第二脳を構築
  - ツール: OpenKB (pip install openkb) + Obsidian
  - リポジトリ: hiroshi57/Claude-Master-Folder（Public）
  - 認証: GitHub Actions WIF（API キー不要）
  - ローカル実行時は `.env` に `LLM_API_KEY` を記入
- **2026-05-07**: openkb コマンドは `C:\Users\hiroshi_takizawa\Obsidian_hub` 内で実行
  - PATH: `~/.bashrc` に `/c/Users/hiroshi_takizawa/AppData/Roaming/Python/Python313/Scripts` 追加済み
- **2026-05-07**: WIF の Console 設定（Phase 1）は未完了
  - 必要: Service Account / Federation Issuer / Federation Rule を Anthropic Console で作成
  - GitHub Secrets に `ANTHROPIC_FEDERATION_RULE_ID` / `ANTHROPIC_ORGANIZATION_ID` / `ANTHROPIC_SERVICE_ACCOUNT_ID` を登録

---

## 進行中プロジェクト（2026-05-07 現在）

### AI 第二脳（Obsidian_hub）
- [x] Obsidian_hub セットアップ（raw/ wiki/ CLAUDE.md）
- [x] OpenKB インストール・設定
- [x] GitHub Actions WIF ワークフロー作成（update-wiki.yml）
- [ ] Anthropic Console WIF 設定（Service Account / Issuer / Rule）
- [ ] GitHub Secrets に WIF 変数を登録
- [ ] `.env` に `LLM_API_KEY` を記入してローカル動作確認
- [ ] `openkb add raw/` で初回 ingest を実行

### AI-info-dashboard (C:\Users\hiroshi_takizawa\AI-info-dashboard)
- [x] 🔧 **ハーネス設計ページ追加** — navbtn-harness・page-harness・PAGE_GROUP_MAP・GROUP_DEFAULTS・renderHarness() 接続（2026-05-07）

### seo-managed-agents ダッシュボード
- [x] ダッシュボード大規模改修（改善策カード・D&Dレポート・OpenAI デザイン）— commit 32f9d7f（2026-05-07）
- [x] プロンプト選択をクライアントごとに localStorage 保存（_savePromptSelection/_loadPromptSelection）— commit 32f9d7f（2026-05-07）
- [x] GA4 / Search Console 実API接続（auth.py・ga4.py・/api/fetch-ga4）— commit 32f9d7f（2026-05-07）
  - ⚠️ **ユーザー手順**: credentials.json を Google Cloud Console から DL → dashboard/ に配置
- [ ] ChatGPT / Gemini 実LLMO調査（OpenAI/Gemini API でプロンプト送信）

---

## Personal Context（個人コンテキスト）

- **ツール環境**: Windows 11、Claude Code、VS Code、Git Bash
- **GitHub**: hiroshi57
- **メール**: takizawa.hiroshi@digitalidentity.co.jp

---

*最終更新: 2026-05-07 (Task #7〜#10 完了)*
