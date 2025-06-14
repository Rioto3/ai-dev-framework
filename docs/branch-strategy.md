# ブランチ戦略・プロジェクト管理

## リポジトリ作成標準フロー

### 必須トランザクション
1. **リポジトリ作成**（main）
2. **develop ブランチ派生**
3. **基本README作成**
4. **ai-roles.yaml テンプレート配置**

## ブランチ命名規則

### 基本構成
- `main` - 本番用（保護）
- `develop` - 開発作業用（デフォルト）

### 機能別ブランチ（大機能のみ）
- `feature/{feature-name}` - UX-AI主導
- `feature/{feature-name}-ui` - UI-AI作業
- `feature/{feature-name}-api` - Backend作業

## 作業管理

### コミットログ中心
- **履歴管理**: Gitコミットで差分・進捗管理
- **明確なメッセージ**: 作業内容を簡潔に記述
- **段階的コミット**: 機能単位での細かいコミット

### Issue運用（軽量）
- **小規模**: Issue不要、コミットログで十分
- **中規模以上**: 大機能のみIssue作成
- **複雑プロジェクト**: 従来の[UX][UI]ラベル運用

## 分業判断

### UX-AI単独
- MVP、シンプルUI
- 小規模拡張機能
- プロトタイプ

### 分業必要
- 高級UI要求
- 複雑なバックエンド
- 大規模システム

## ブランチ運用例

```
main ← 本番
develop ← 作業メイン
├── feature/user-auth（大機能時のみ）
└── feature/user-auth-ui（UI-AI連携時）
```

## 作業フロー

1. **プロジェクト開始**: リポジトリ作成 → develop作成
2. **実装**: develop で直接作業
3. **分業時**: feature ブランチ派生
4. **完成**: main へマージ
