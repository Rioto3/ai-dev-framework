# AI Development Framework

AIチーム構成による効率的なプロジェクト開発フレームワーク

## 概要

従来の開発手法の限界を突破し、AI専門チームによる自動化・最適化を実現するメタ開発フレームワーク。

### 核心思想

- **UI重視**: ユーザー体験が最優先、AIの効率化はそれを支える手段
- **AI役割分離**: UX設計AI、UI実装AI、文書作成AIなど専門特化
- **プロジェクト×AI構成**: 1プロジェクトに複数AI、ドキュメントベースで役割定義

## アーキテクチャ

```
Project A
├── UX Designer AI (ユーザー体験設計)
├── UI Developer AI (実装・コーディング)
├── Documentation AI (文書作成)
└── Feedback AI (分析・改善提案)
```

### ブランチ戦略
- AIごとの責任ブランチ: `uxai/`, `devai/`, `docai/`
- タスクベース派生: `uxai/landing-flow-v2`
- GitHub Issue連携によるMVP駆動開発

## 使用方法

### 1. 新規プロジェクトへの適用

```bash
# テンプレートをコピー
cp -r templates/project-init/ /path/to/new-project/

# AI役割を定義
vi ai-roles.yaml
```

### 2. AI役割設定

各プロジェクトで`ai-roles.yaml`を編集し、担当範囲を明確化

### 3. GitHub連携

Issue作成、ブランチ管理、PR統合を自動化

## 構成

- `templates/` - 新規プロジェクト用テンプレート
- `scripts/` - 自動化スクリプト
- `docs/` - 設計思想・運用ガイド

## 目標

技術的制約ではなく「設計と意味」で差別化する開発体制の実現

---

**開発者**: 森谷亮太 (RYOTA MORIYA)  
**アーキテクト・サポート**: Claude (Anthropic)
