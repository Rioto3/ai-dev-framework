# AI Development Framework

AIチーム構成による効率的なプロジェクト開発フレームワーク

## 概要

従来の開発手法の限界を突破し、AI専門チームによる自動化・最適化を実現するメタ開発フレームワーク。**IT開発のみならず、建築・飲食・イベント企画など、あらゆる分野のプロジェクト管理に適用可能。**

### 核心思想

- **UX重視**: ユーザー体験が最優先、AIの効率化はそれを支える手段
- **AI役割分離**: UX-AI、UI-AI、Backend-AIなど専門特化
- **プロジェクト×AI構成**: 1プロジェクトに複数AI、ドキュメントベースで役割定義
- **GitHub as Backend**: GitHubをバックエンドとし、AIを介した読み書きでUI的に能力拡張
- **AI-First Design**: 人間の細部デザイン判断を削減、フレームワーク効果を最大化
- **汎用設計**: バックエンド領域を抽象化し、任意分野への適用を可能に

## アーキテクチャ

### IT開発の場合
```
Project A
├── UX-AI (体験設計・統括・文書作成)
├── UI-AI (スタイリング・CSS実装)
└── Backend-AI (DB・API・SaaS連携)
```

### 他分野の例
```
建築プロジェクト
├── UX-AI (住民体験・動線設計・統括)
├── Design-AI (建築デザイン・美観)
└── Construction-AI (施工計画・材料選定)

飲食店プロジェクト
├── UX-AI (客体験・オペレーション設計・統括)
├── Interior-AI (内装・雰囲気作り)
└── Kitchen-AI (厨房設計・メニュー開発)
```

## 前提条件

- **GitHub基本操作**: リポジトリ作成、Issue管理、ブランチ操作
- **AI使用者のリテラシ**: フレームワーク対象分野の基礎知識
- **原則**: AIが扱う範囲において、使用者も同等の最低限リテラシを保持

## ブランチ戦略

軽量運用による効率重視：

- `main` - 本番リリース用（保護）
- `develop` - 開発作業用（デフォルト）

大きな転換が必要な場合のみブランチ派生。通常はdevelopで直接作業。

### ブランチ戦略
- UX-AIメインブランチ: `feature/login-system`
- 派生ブランチ: `feature/login-system-ui`, `feature/login-system-api`
- GitHub Issue連携によるMVP駆動開発

## AI統合

**主要AI**: Claude (Anthropic)  
**操作UI**: https://claude.ai/chat/9c4ba6de-6fa9-4089-83ad-81c3d6bb1cdd

このリポジトリは主にAI経由で読み書きされ、GitHubを透明なバックエンドとして活用。

## 使用方法

### 1. 新規プロジェクトへの適用

```bash
# テンプレートをコピー
cp templates/ai-roles.yaml /path/to/new-project/

# AI役割を定義
vi ai-roles.yaml
```

### 2. AI役割設定

各プロジェクトで`ai-roles.yaml`を編集し、担当範囲を明確化

### 3. GitHub連携

Issue作成、ブランチ管理、PR統合を自動化

## 構成

- `templates/` - 新規プロジェクト用テンプレート
- `docs/` - 設計思想・運用ガイド

## 目標

技術的制約ではなく「設計と意味」で差別化する開発体制の実現

---

**開発者**: 森谷亮太 (RYOTA MORIYA)  
**アーキテクト・サポート**: Claude (Anthropic)
