# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is `gh-ext-manage`, a GitHub CLI extension for declarative management of GitHub CLI extensions. The extension is written in Japanese documentation but provides functionality for:

- Installing extensions from configuration files
- Syncing manually installed extensions to configuration
- Managing extension versions and aliases
- Updating extensions individually or in bulk

## Project Structure

This appears to be a minimal GitHub CLI extension repository that currently only contains:

- `README.md` - Japanese documentation explaining the extension's purpose and usage
- Git repository files

The actual extension code (shell scripts, manifest files, etc.) that would typically be present in a GitHub CLI extension are not yet implemented.

## Key Commands

Based on the README documentation, the extension is designed to support these commands:

- `gh ext-manage list` - List installed extensions
- `gh ext-manage install` - Install extensions from config file
- `gh ext-manage sync` - Sync manually installed extensions to config
- `gh ext-manage update [extension]` - Update extensions
- `gh ext-manage help` - Show help
- `gh ext-manage version` - Show version

## Dependencies

- GitHub CLI (gh)
- jq (for JSON processing)

## Development Notes

This repository is in early stages - it contains documentation but lacks the actual implementation files typically found in GitHub CLI extensions:

- No manifest.yml file (required for GitHub CLI extensions)
- No executable script files
- No configuration or test files

When implementing this extension, you'll need to create the standard GitHub CLI extension structure with appropriate shell scripts and manifest files.

## Code Quality

All shell scripts should pass shellcheck validation. Run `shellcheck` on any shell script files before committing changes.

All Markdown files should pass markdownlint-cli2 validation. Run `markdownlint-cli2` on Markdown files before committing changes.

