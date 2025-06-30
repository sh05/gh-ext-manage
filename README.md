# gh-ext-manage

GitHub CLI Extension Manager - A tool for declarative management of GitHub CLI extensions

## Overview

`gh-ext-manage` is a GitHub CLI extension that enables declarative management of GitHub CLI extensions.

Key features:
- Batch installation of extensions from configuration files
  - Supports alias configuration
  - Version management
- Sync manually installed extensions to configuration files

## Installation

```bash
gh extension install sh05/gh-ext-manage
```

## Dependencies

- [GitHub CLI](https://cli.github.com/) (gh)
- [jq](https://stedolan.github.io/jq/) (for JSON processing)

## Usage

### Basic Commands

```bash
# List installed extensions
gh ext-manage list

# Install extensions from config
gh ext-manage install

# Sync manually installed extensions to config file
gh ext-manage sync

# Update all extensions
gh ext-manage update

# Update specific extension
gh ext-manage update <extension-name>

# Show help
gh ext-manage help

# Show version information
gh ext-manage version
```

## Features

- 📦 **Extension Listing**: Display detailed information of installed extensions (`list`)
- 📥 **Extension Installation**: Batch install extensions from configuration file (`install`)
- 🔄 **Configuration Sync**: Sync manually installed extensions to configuration file (`sync`)
- ⬆️ **Extension Updates**: Update extensions individually or in batch (`update`)
- ⚙️ **Declarative Management**: Support for alias configuration and version management
- ✨ **Intuitive UI**: Clear output with emojis and colors

## Configuration

The configuration file is located at `~/.config/gh-ext-manage/config.json`.

### Example Configuration

```json
{
  "extensions": [
    {"repo": "cli/gh-copilot"},
    {"repo": "github/gh-actions"},
    {"repo": "dlvhdr/gh-dash", "alias": "dashboard"}
  ]
}
```

## Language Support

This extension supports both English and Japanese languages. The language is automatically detected from your system locale:

- English (default): `LANG=en_US.UTF-8` or `LC_ALL=en_US.UTF-8`
- Japanese: `LANG=ja_JP.UTF-8` or `LC_ALL=ja_JP.UTF-8`

You can also force a specific language by setting the environment variable:

```bash
# Force English
LANG=en_US.UTF-8 gh ext-manage list

# Force Japanese
LANG=ja_JP.UTF-8 gh ext-manage list
```

## Documentation

- [日本語版 README](README_ja.md) - Japanese documentation

## License

MIT License