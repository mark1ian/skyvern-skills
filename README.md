# Skyvern Skills Package

Canonical distribution source for Skyvern skills and Claude Code plugin installation.

This repository packages Skyvern browser automation for agent workflows and provides a single public source that can be used across Claude Code and cross-agent skills tooling.

## What's Included

- `.claude-plugin/marketplace.json` — Claude Code marketplace definition
- `plugins/skyvern-browser-automation/.claude-plugin/plugin.json` — plugin package metadata
- `plugins/skyvern-browser-automation/skills/skyvern-browser-automation/SKILL.md` — browser automation skill
- `plugins/skyvern-browser-automation/.mcp.json` — MCP server configuration

This repository serves as both a Claude Code plugin marketplace source and a skills package source for cross-agent installation flows.

## Requirements

- [Claude Code](https://claude.ai/claude-code) CLI
- A Skyvern account and API key ([skyvern.com](https://www.skyvern.com))

## Install in Claude Code

Add this repository as a marketplace source:

```bash
/plugin marketplace add mark1ian/skyvern-skills
```

Then install the plugin:

```bash
/plugin install skyvern-browser-automation
```

## Repository Layout

```
skyvern-skills/
├── .claude-plugin/marketplace.json
└── plugins/
    └── skyvern-browser-automation/
        ├── .claude-plugin/plugin.json
        ├── .mcp.json
        └── skills/
            └── skyvern-browser-automation/
                └── SKILL.md
```
