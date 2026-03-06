# Crossbill Claude Plugin

This is a Claude Code plugin for the Crossbill reading app.

## Project structure

- `.claude-plugin/plugin.json` — plugin manifest (name, version, metadata)
- `.mcp.json` — MCP server config, expects `crossbill-mcp` to be installed via pip
- `skills/` — plugin skills (each skill is a directory with a `SKILL.md`)

## Dependencies

- The `crossbill-mcp` package from `../crossbill-web/mcp-server/` must be installed (`pip install ./mcp-server`)
- Requires environment variables: `CROSSBILL_URL`, `CROSSBILL_EMAIL`, `CROSSBILL_PASSWORD`

## Testing locally

```bash
claude --plugin-dir .
```
