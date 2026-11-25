# Aldena integrations

Plugins that connect AI tools to [Aldena](https://aldena.ai). Aldena is a cloud runtime for your team's Claude Code or Codex. New tickets start runs in your own sandbox, and only decisions reach your inbox.

Each integration lives in its own folder, with a README that covers what it holds, how to install it and what data it sends.

| Folder | For |
| ------ | --- |
| [`claude/`](claude/) | Claude Code, claude.ai and Cowork |

## Claude

This repo is also a Claude plugin marketplace. In a Claude Code session:

```text
/plugin marketplace add aldena-ai/integrations
/plugin install aldena@aldena
```

Or from a shell:

```bash
claude plugin marketplace add aldena-ai/integrations
claude plugin install aldena@aldena
```

Then run `/mcp`, pick `aldena` and sign in. [claude/README.md](claude/README.md) covers claude.ai and Cowork too.

## Any other MCP client

Until there is a plugin for your tool, point it at Aldena's MCP server, `https://mcp.aldena.ai/mcp`. The [MCP server docs](https://docs.aldena.ai/mcp) show the setup for Cursor, VS Code and other clients, with OAuth or an API key.

## License

MIT. See [LICENSE](LICENSE).
