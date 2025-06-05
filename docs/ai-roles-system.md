# AI役割定義システム

## AI命名規則

- **UX-AI**: ユーザー体験設計・プロジェクト統括
- **UI-AI**: ユーザーインターフェース実装・スタイリング
- **Doc-AI**: 文書作成・説明生成
- **Backend-AI**: API・データベース設計（参考情報）

## ai-roles.yaml ファイル

各プロジェクトのルートに配置し、AI役割を定義。

### 基本構造
```yaml
project: "プロジェクト名"
description: "プロジェクト概要"
roles:
  ux-ai:
    responsibility: "責任範囲"
    input: "入力形式"
    output: "出力形式"
    tools: ["HTML", "JS"]
  ui-ai:
    responsibility: "責任範囲"
    input: "入力形式" 
    output: "出力形式"
    tools: ["CSS", "Bootstrap"]
```

### 設定パターン

**MVP/シンプル**: UX-AIのみ
**標準**: UX-AI + UI-AI
**複雑**: UX-AI + UI-AI + Backend参考

## 使用方法

1. 新規プロジェクトでai-roles.yamlを作成
2. プロジェクト要件に応じて役割定義を調整
3. 各AIがファイルを参照して作業実行
