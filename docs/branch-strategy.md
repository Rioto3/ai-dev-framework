# ブランチ戦略・Issue運用

## ブランチ命名規則

### UXAIメインブランチ
- `feature/{feature-name}` - 新機能開発
- `fix/{bug-name}` - バグ修正
- `improve/{target}` - 改善作業

### 派生ブランチ
- `{type}/{feature-name}-ui` - UIAI作業用
- `{type}/{feature-name}-api` - Backend作業用
- `{type}/{feature-name}-doc` - 文書作成用

## 作業フロー

1. **Issue作成** - UXAIがタスク定義
2. **UXAIブランチ** - developから派生、HTML/JSモック作成
3. **派生ブランチ** - 必要に応じてUXAIブランチから派生
4. **統合** - 完成後にdevelopへマージ

## Issue管理

### ラベル体系
- `uxai` - UX設計・統括
- `uiai` - UI実装
- `backend` - API/データベース
- `documentation` - 文書作成

### Issue例
```
#1 [UXAIメイン] ユーザーログイン機能の実装
#2 [UIAI] ログイン画面のスタイリング
#3 [Backend] 認証API実装
```

## PR運用

基本はdirect commit、大きな統合時のみPR使用。
