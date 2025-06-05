# AI役割定義システム

## AI命名規則

- **UX-AI**: ユーザー体験設計・プロジェクト統括・ルーティング・文書作成
- **UI-AI**: ユーザーインターフェース実装・スタイリング
- **Backend-AI**: DB・API・SaaS連携・決済・外部リソース管理

## ai-roles.yaml ファイル構造

### 必須セクション
- `project`: プロジェクト名・概要
- `priority`: 作業優先順位（ux-first推奨）
- `roles`: 各AI責任・入出力・ツール定義

### AI間連携セクション
- `handoff`: Issue経由の連携方法
- `naming-convention`: Issueラベル規則
- `workflow`: 作業フロー定義

## Issue連携システム

### 命名規則
```
[UX] タスク説明
[UI] タスク説明 (ref: #親Issue)
[API] タスク説明 (ref: #親Issue)
```

### ワークフロー
1. UX-AI → 統括・判断
2. UX-AI → UI-AI/Backend-AI（Issue作成・成果物添付）
3. 完了時Issue close + コミット

## ファイル使用方法

1. `templates/ai-roles.yaml`をプロジェクトルートにコピー
2. プロジェクト要件に応じて調整
3. 各AIがファイル参照して自律作業
4. Issue経由で連携・進捗管理
