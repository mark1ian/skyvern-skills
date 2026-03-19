# Skyvern Skills Package

Canonical distribution source for Skyvern skills and Claude Code plugin installation.

This repository packages Skyvern browser automation for agent workflows and provides a single public source that can be used across Claude Code and cross-agent skills tooling.

## What’s Included

This repository includes:

- a Claude Code marketplace definition in `.claude-plugin/marketplace.json`
- a plugin package in `plugins/skyvern-browser-automation/.claude-plugin/plugin.json`
- a Skyvern browser automation skill in `plugins/skyvern-browser-automation/skills/skyvern-browser-automation/SKILL.md`
- an MCP configuration in `plugins/skyvern-browser-automation/.mcp.json`

Together, these files allow the same repository to serve as both:
- a Claude Code plugin marketplace source
- a skills package source for cross-agent installation flows

## Install in Claude Code

Add this repository as a marketplace in Claude Code:

```bash
/plugin marketplace add mark1ian/skyvern-skills
