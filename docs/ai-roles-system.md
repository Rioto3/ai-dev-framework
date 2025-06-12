# AI役割定義システム

## AI命名規則

- **UX-AI**: ユーザー体験設計・プロジェクト統括・JSXモック作成・文書作成
- **Backend-AI**: 分野特化実装・API・DB・SaaS連携・専門知識処理

## ai-roles.yaml ファイル構造

### 必須セクション
- `project`: プロジェクト名・概要
- `priority`: 作業優先順位（ux-first推奨）
- `roles`: 各AI責任・入出力・ツール定義

### 作業管理セクション
- `workflow`: リポジトリ作成・開発・連携フロー
- `github`: ブランチ設定・命名規則

## 軽量運用モデル

### 小規模プロジェクト
- **UX-AI単独**: MVP・シンプルUI
- **管理**: コミットログ中心
- **ブランチ**: develop のみ

### 中規模プロジェクト
- **分業**: 必要時のみBackend-AI連携
- **管理**: コミットログ + 最小限Issue
- **ブランチ**: feature 派生

### 大規模プロジェクト
- **完全分業**: 従来の[UX][API]ラベル運用
- **管理**: 詳細Issue + PR連携
- **ブランチ**: 複数feature並行

## html.to.design統合

### Claude → Figma直接連携
- **JSX作成**: UX-AIがArtifact完成度95%
- **Figma描画**: html.to.design MCP活用
- **制約**: 月10回制限（無料版）

### Figma → 実装連携
- **読み取り**: figma-developer-mcp活用
- **Backend-AI**: Figma + Artifact両方で実装
- **デザイン調整**: 人間がFigmaで微調整

## ファイル使用方法

1. `templates/ai-roles.yaml`をプロジェクトルートにコピー
2. プロジェクト要件に応じて調整
3. 各AIがファイル参照して自律作業
4. コミットログまたはIssueで進捗管理

## リポジトリ作成標準フロー

### UX-AI必須手順
1. **リポジトリ作成**（main）
2. **develop ブランチ派生**
3. **基本README作成**
4. **ai-roles.yaml配置**

### 作業開始
- **develop** での直接作業
- **明確なコミットメッセージ**
- **段階的実装**