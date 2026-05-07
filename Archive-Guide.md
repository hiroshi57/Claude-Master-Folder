# Archive-Guide.md
> Claude Master Folder のバックアップ・アーカイブ手順書

---

## なぜアーカイブが必要か

Claude は Memory.md・Context.md を自動更新します。  
このとき、意図しない上書きや誤った変更が発生することがあります。  
バックアップなしでは、**積み上げたコンテキストが一瞬で消える**リスクがあります。

アーカイブは「保険」です。週1回の作業で、数ヶ月分のナレッジを守れます。

---

## 週次アーカイブ手順（毎週行うこと）

### Step 1: フォルダをまるごとコピー

```
コピー元: C:\Users\hiroshi_takizawa\Claude Master Folder\
コピー先: C:\Users\hiroshi_takizawa\Claude Archives\YYYY-MM-DD\
```

**Windows でのコピー方法（エクスプローラー）:**
1. `Claude Master Folder` を右クリック →「コピー」
2. `Claude Archives` フォルダを開く（なければ新規作成）
3. 右クリック →「貼り付け」
4. フォルダ名を `2026-05-07` のように日付でリネーム

**コマンドプロンプトでのコピー:**
```cmd
xcopy "C:\Users\hiroshi_takizawa\Claude Master Folder" "C:\Users\hiroshi_takizawa\Claude Archives\2026-05-07" /E /I
```

### Step 2: アーカイブフォルダを Claude からアクセス不可の場所に移動

**重要**: Claude Code が読み書きできるフォルダにアーカイブを置かないこと。  
推奨保存場所:
- `OneDrive\Claude Archives\` （クラウド同期で安全）
- 外付けHDD・USBドライブ
- `C:\Users\hiroshi_takizawa\AppData\` 配下（Claude は通常アクセスしない）

### Step 3: 保存確認

コピー先のフォルダを開き、以下4ファイルが存在することを確認:
- [ ] `Instructions.md`
- [ ] `Memory.md`
- [ ] `Context.md`
- [ ] `Archive-Guide.md`

---

## アーカイブに含めるべきもの

| 含めるもの | 理由 |
|-----------|------|
| `Instructions.md` | Claude へのルール定義 |
| `Memory.md` | 蓄積された好み・訂正・パターン |
| `Context.md` | プロジェクト固有の文脈 |
| プロジェクト固有フォルダ | 追加で作成したコンテキストファイル |
| Obsidian Wiki（任意） | 第二脳のスナップショット |

---

## 何かが壊れたときの復元手順

### 症状例
- Memory.md の内容が消えた・おかしくなった
- Context.md が上書きされて別の内容になった
- Instructions.md のルールが勝手に変わった

### 復元手順

1. `Claude Archives\` から最新の日付フォルダを開く
2. 問題のあるファイルをコピー
3. `Claude Master Folder\` に貼り付けて上書き
4. Claude に「Memory.md を読み直して」と伝える

```
復元コマンド例:
copy "C:\Users\hiroshi_takizawa\Claude Archives\2026-05-07\Memory.md" "C:\Users\hiroshi_takizawa\Claude Master Folder\Memory.md"
```

---

## アーカイブスケジュール（推奨）

| タイミング | 作業 |
|-----------|------|
| **毎週月曜日** | 週次アーカイブ（必須） |
| 大きな変更後 | 随時アーカイブ |
| 月1回 | 古いアーカイブの整理（3ヶ月以上前は削除可） |

---

## 推奨フォルダ構造

```
C:\Users\hiroshi_takizawa\
├── Claude Master Folder\          ← Claude が読み書きする（現在進行形）
│   ├── Instructions.md
│   ├── Memory.md
│   ├── Context.md
│   └── Archive-Guide.md
│
└── Claude Archives\               ← Claude がアクセスしない（バックアップ）
    ├── 2026-05-07\
    │   ├── Instructions.md
    │   ├── Memory.md
    │   ├── Context.md
    │   └── Archive-Guide.md
    ├── 2026-05-14\
    └── 2026-05-21\
```

---

*最終更新: 2026-05-07*
