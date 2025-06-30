# gh-ext-manage

GitHub CLI Extension Manager - GitHub CLI拡張を簡単に管理するためのツール

## 概要

`gh-ext-manage`は、GitHub CLI拡張の宣言的な管理を可能にするGitHub CLI拡張です。

- 設定ファイルに記述されている拡張の一括インストール
  - 下記も実現します
    - エイリアス設定
    - バージョン管理
- 手動でインストールした拡張の設定ファイルへの反映

## インストール

```bash
gh extension install sh05/gh-ext-manage
```

## 必要な依存関係

- [GitHub CLI](https://cli.github.com/) (gh)
- [jq](https://stedolan.github.io/jq/) (JSON処理用)

## 使用方法

### 基本コマンド

```bash
# インストール済み拡張の一覧表示
gh ext-manage list

# 拡張のインストール
gh ext-manage install

# インストール済み拡張の設定ファイルへの同期
gh ext-manage sync

# 全拡張の更新
gh ext-manage update

# 特定拡張の更新
gh ext-manage update <拡張名>

# ヘルプの表示
gh ext-manage help

# この拡張のバージョン情報の表示
gh ext-manage version
```

## 機能

- 📦 **拡張一覧表示**: インストール済み拡張の詳細情報を表示 (`list`)
- 📥 **拡張インストール**: 設定ファイルに記述された拡張を一括インストール (`install`)
- 🔄 **設定同期**: 手動でインストールした拡張を設定ファイルに反映 (`sync`)
- ⬆️ **拡張更新**: 個別または一括で拡張を更新 (`update`)
- ⚙️ **宣言的管理**: エイリアス設定やバージョン管理に対応
- ✨ **直感的UI**: 絵文字とカラーを使った分かりやすい出力

## ライセンス

MIT License

