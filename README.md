# Crossbill Claude Plugin

Claude Code plugin for [Crossbill](https://crossbill.app) reading app integration. Provides skills and MCP tools for interacting with your reading data — books, highlights, flashcards, and reading sessions.

## Prerequisites

- [Claude Code](https://claude.com/claude-code) v1.0.33 or later
- [crossbill-mcp](https://github.com/crossbill/crossbill-web/tree/main/mcp-server) server installed

## Install the MCP server

The plugin requires the `crossbill-mcp` server to be installed and available in your PATH.

From the [crossbill-web](https://github.com/crossbill/crossbill-web) repository:

```bash
pip install ./mcp-server
```

Set the required environment variables:

```bash
export CROSSBILL_URL="https://your-crossbill-instance.com"
export CROSSBILL_EMAIL="your-email@example.com"
export CROSSBILL_PASSWORD="your-password"
```

## Install the plugin

### Local development

```bash
claude --plugin-dir /path/to/claude-plugin
```

### Permanent installation

Once the plugin is available in a marketplace:

```bash
claude plugin install crossbill
```

## Skills

| Skill | Description |
|:------|:------------|
| `/crossbill:reading-quiz` | Quiz yourself on recently read material |

## Plugin structure

```
claude-plugin/
├── .claude-plugin/
│   └── plugin.json        # Plugin manifest
├── .mcp.json              # MCP server configuration
└── skills/
    └── reading-quiz/
        └── SKILL.md       # Reading quiz skill
```
