# 初めてのCodex — PowerShell Launch Guide

OpenAIのCLIコーディングエージェント「Codex」を、Windows PowerShellから初めて立ち上げる手順をスクリーンショット付きで解説するスタティックページ。

GitHub Pagesで公開: <!-- TODO: 公開URLを記入 -->

## 構成

```
.
├── index.html           ガイド本体（GitHub Pagesのエントリポイント）
├── assets/
│   ├── codex_pwsh_search.png    Step 1: Windows検索からPowerShell起動
│   ├── codex_npm_install.png    Step 2: npm install -g @openai/codex
│   ├── codex_welcome.png        Step 3: 認証メニュー
│   └── codex_ready.png          Step 4: サインイン後の起動画面
├── .nojekyll            JekyllをスキップしてそのままHTMLを公開
└── README.md
```

## 公開手順（GitHub Pages）

```bash
# このディレクトリで初期化
git init
git add .
git commit -m "Initial commit: Codex launch guide"

# GitHub にリポジトリ作成（gh CLI）
gh repo create codex-launch-guide --public --source=. --remote=origin --push

# GitHub Pages を main ブランチのルートで有効化
gh api -X POST /repos/:owner/codex-launch-guide/pages \
  -f source[branch]=main -f source[path]=/
```

公開URLは `https://<username>.github.io/codex-launch-guide/` 。

## ライセンス

スクリーンショットの著作権はOpenAI / Microsoftに帰属。本ガイドの文章はAppTalentHub。
