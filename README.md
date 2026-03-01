# フロントセミナー着座特典

フロントセミナー参加者向け特典コンテンツのプロジェクトです。

## 概要

このプロジェクトは [TAISUN v2](https://github.com/taiyousan15/taisun_agent) をベースに構築されています。
68スキル・85エージェント・227 MCPツールを統合した開発・マーケティングプラットフォームを利用して特典コンテンツを制作します。

## セットアップ

### 前提条件

- Node.js 18.x 以上
- `c:\dev\taisun_agent` がセットアップ済みであること

### 手順

```bash
# taisun_agent のビルドが済んでいることを確認
cd c:\dev\taisun_agent
npm install
npm run build:all
```

Claude Code でこのディレクトリを開くと、以下が自動的に有効になります：

- **MCP サーバー**: taisun-proxy（227ツール）、playwright、context7
- **エージェント**: 85種（`.claude/agents/`）
- **スキル**: 68種（`.claude/skills/`）
- **スラッシュコマンド**: 80種以上（`.claude/commands/`）
- **13層防御システム**: ワークフロー逸脱防止フック

## プロジェクト構成

```
.
├── CLAUDE.md              # Claude Code 設定（taisun_agent の CLAUDE.md をインポート）
├── README.md              # このファイル
└── .claude/
    ├── settings.json      # MCP サーバー・フック設定
    ├── agents/            # 85エージェント定義（taisun_agent より）
    ├── skills/            # 68スキル定義（taisun_agent より）
    ├── commands/          # スラッシュコマンド（taisun_agent より）
    ├── hooks/             # 防御システム（taisun_agent より）
    └── rules/             # ルール定義（taisun_agent より）
```

## 利用方法

Claude Code でこのプロジェクトを開き、スラッシュコマンドを使用します：

```
/lp-normal       # LP作成
/copywriting     # コピーライティング
/mega-research   # 深層リサーチ
/taiyou-auto     # 太陽スタイル自動生成
```
