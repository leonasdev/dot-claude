# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal Claude Code plugins repository (`dot-claude`) that contains custom slash commands for Claude Code. The plugins extend Claude Code's functionality with git-related automation.

## Architecture

```
.claude-plugin/marketplace.json   # Root manifest defining available plugins
plugins/
  git-commands/                   # Git-related commands plugin
    .claude-plugin/plugin.json    # Plugin metadata
    commands/                     # Slash command definitions (markdown files)
```

### Plugin Structure

- **Marketplace manifest** (`.claude-plugin/marketplace.json`): Defines the collection of plugins with name, description, owner info, and plugin sources
- **Plugin manifest** (`plugins/<name>/.claude-plugin/plugin.json`): Individual plugin metadata (name, version, author)
- **Commands** (`plugins/<name>/commands/*.md`): Markdown files defining slash commands with YAML frontmatter

### Command File Format

Commands are markdown files with:
- YAML frontmatter containing `description` and optional `model` override
- Shell command interpolation using `!`backtick`command`backtick`` syntax for dynamic context
- Task instructions in the markdown body

## Current Plugins

**git-commands**: Git commit and PR generation commands
- `/commit` - Haiku 4.5 for quick single-line commit subjects
- `/commit+` - Sonnet 4.5 for detailed commit messages
- `/commit++` - Opus 4.5 for comprehensive commit messages
- `/pr` - Generate PR title and body
