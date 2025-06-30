# gh-ext-manage

GitHub CLI Extension Manager - GitHub CLI拡張の宣言的管理ツール

## 概要

`gh-ext-manage`は、GitHub CLI拡張の宣言的管理を可能にするGitHub CLI拡張です。

主な機能:
- 設定ファイルからの拡張の一括インストール
  - エイリアス設定のサポート
  - バージョン管理
- 手動でインストールした拡張の設定ファイルへの同期

## インストール

```bash
gh extension install sh05/gh-ext-manage
```

## 依存関係

- [GitHub CLI](https://cli.github.com/) (gh)
- [jq](https://stedolan.github.io/jq/) (JSON処理用)

## 使用方法

### 基本コマンド

```bash
# インストール済み拡張の一覧表示
gh ext-manage list

# 設定から拡張をインストール
gh ext-manage install

# 手動でインストールした拡張を設定ファイルに同期
gh ext-manage sync

# 全拡張の更新
gh ext-manage update

# 特定拡張の更新
gh ext-manage update <拡張名>

# ヘルプの表示
gh ext-manage help

# バージョン情報の表示
gh ext-manage version
```

## 機能

- 📦 **拡張一覧表示**: インストール済み拡張の詳細情報を表示 (`list`)
- 📥 **拡張インストール**: 設定ファイルに記述された拡張を一括インストール (`install`)
- 🔄 **設定同期**: 手動でインストールした拡張を設定ファイルに反映 (`sync`)
- ⬆️ **拡張更新**: 個別または一括で拡張を更新 (`update`)
- ⚙️ **宣言的管理**: エイリアス設定やバージョン管理に対応
- ✨ **直感的UI**: 絵文字とカラーを使った分かりやすい出力

## 設定

設定ファイルは `~/.config/gh-ext-manage/config.json` に配置されます。

### 設定例

```json
{
  "extensions": [
    {"repo": "github/gh-copilot"},
    {"repo": "dlvhdr/gh-dash", "alias": "dashboard"},
    {"repo": "mislav/gh-branch"},
    {"repo": "vilmibm/gh-screensaver"}
  ]
}
```

## 言語サポート

この拡張は英語と日本語に対応しています。言語はシステムのロケールから自動検出されます:

- 英語 (デフォルト): `LANG=en_US.UTF-8` または `LC_ALL=en_US.UTF-8`
- 日本語: `LANG=ja_JP.UTF-8` または `LC_ALL=ja_JP.UTF-8`

環境変数を設定して特定の言語を強制することも可能です:

```bash
# 英語を強制
LANG=en_US.UTF-8 gh ext-manage list

# 日本語を強制
LANG=ja_JP.UTF-8 gh ext-manage list
```

## ドキュメント

- [English README](README.md) - English documentation

## ライセンス

MIT License