# claude-code-test

GitHub環境テンプレートプロジェクト

## ブランチ戦略

このプロジェクトは **Git Flow** ブランチ戦略を採用しています。

### メインブランチ

- **`main`** - 本番環境用のブランチ。本番リリース可能な状態のコードのみ
- **`develop`** - 開発用のメインブランチ。すべての機能開発はここにマージされます

### サポートブランチ

- **`feature/*`** - 新機能開発用
  - 分岐元: `develop`
  - マージ先: `develop`
  - 例: `feature/user-authentication`

- **`release/*`** - リリース準備用
  - 分岐元: `develop`
  - マージ先: `main` と `develop`
  - 例: `release/1.0.0`

- **`hotfix/*`** - 緊急バグ修正用
  - 分岐元: `main`
  - マージ先: `main` と `develop`
  - 例: `hotfix/critical-security-fix`

## 開発フロー

### 新機能を追加する場合

```bash
# developブランチから最新の状態を取得
git checkout develop
git pull origin develop

# 機能ブランチを作成
git checkout -b feature/your-feature-name

# 開発・コミット
git add .
git commit -m "feat: add your feature"

# プッシュしてPR作成
git push origin feature/your-feature-name
```

### リリースする場合

```bash
# リリースブランチを作成
git checkout -b release/1.0.0 develop

# バージョン番号の更新など

# mainにマージ
git checkout main
git merge --no-ff release/1.0.0
git tag -a 1.0.0

# developにもマージ
git checkout develop
git merge --no-ff release/1.0.0

# リリースブランチを削除
git branch -d release/1.0.0
```

## プロジェクト構造

```
.
├── .github/
│   ├── workflows/          # GitHub Actions ワークフロー
│   │   ├── ci.yml         # CI パイプライン
│   │   └── deploy.yml     # デプロイメント
│   ├── ISSUE_TEMPLATE/    # Issue テンプレート
│   │   ├── bug_report.md
│   │   ├── feature_request.md
│   │   └── config.yml
│   └── PULL_REQUEST_TEMPLATE.md
├── CONTRIBUTING.md        # コントリビューションガイド
├── CODE_OF_CONDUCT.md    # 行動規範
├── SECURITY.md           # セキュリティポリシー
└── README.md             # このファイル
```

## コントリビューション

コントリビューションを歓迎します！詳細は [CONTRIBUTING.md](CONTRIBUTING.md) をご覧ください。

## ライセンス

MIT License

## お問い合わせ

質問や提案がある場合は、[Issue](https://github.com/Makoto38710/claude-code-test/issues) または [Discussion](https://github.com/Makoto38710/claude-code-test/discussions) を作成してください。
