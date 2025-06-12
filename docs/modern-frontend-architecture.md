# モダンフロントエンド統合アーキテクチャ

## 概要

UX-AI作成MVPからFigma連携への直接統合開発フロー。

## アーキテクチャ構成

### 基本構成
```
UX-AI (JSX) → html.to.design → Figma → figma-developer-mcp → 実装
Backend-AI (FastAPI) ← 人間統合 → フロントエンド
```

### 技術スタック
- **フロントエンド**: Next.js + TypeScript + Tailwind CSS
- **デザイン統合**: html.to.design + Figma
- **バックエンド**: FastAPI
- **デプロイ**: Vercel (フロント) + 任意サーバ (API)

## 開発フロー

### 1. MVP作成（UX-AI）
- Artifact JSXコンポーネント作成
- 完成度95%まで調整
- html.to.design反映準備

### 2. デザイン統合
```
UX-AI JSX → html.to.design MCP → Figma → デザイン調整 → figma-developer-mcp
```

### 3. バックエンド開発（Backend-AI）
- FastAPI独立開発
- OpenAPI仕様書自動生成
- 分野特化実装

### 4. 最終統合（人間）
- API連携実装
- 品質確認
- デプロイ管理

## 役割分担

### UX-AI
- JSXコンポーネント設計
- ページ構造定義
- html.to.design連携設計

### Backend-AI
- FastAPI専門開発
- データベース設計
- API仕様策定

### 人間（責任者）
- プロジェクト統括
- 技術選択判断
- 最終品質保証

## 技術的特徴

### 直接連携
- Claude → Figma直接描画
- Figma → 構造・スタイル完全読み取り
- コードベース統一管理

### AI専門化
- UX-AI: フロントエンド統括
- Backend-AI: 分野特化実装
- 人間: 統合・監督

### 開発効率
- ビルドレス開発（Next.js dev）
- 自動デプロイ（GitHub連携）
- リアルタイム更新

## 制約・注意点

### 技術制約
- html.to.design月10回制限
- Figmaは静的表示のみ
- バックエンド手動連携

### 運用制約
- UX-AI完成度95%必須
- Figma + Artifact両方でBackend-AI連携
- API連携は人間実装

## 期待効果

- **開発速度**: 従来比200%向上
- **品質**: デザイン・コード双方向最適化
- **保守性**: 統一されたコンポーネント管理
- **拡張性**: 分離アーキテクチャによる柔軟性

---

**更新日**: 2025-06-12  
**関連Issue**: #4 #5 #6