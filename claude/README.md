# Aldena plugin for Claude

Aldena is a cloud runtime for your team's Claude Code or Codex. New tickets start runs in your own sandbox, and only decisions reach your inbox.

With this plugin you can hand a task to one of your project's agents from Claude and ask how the run is going. Claude can also read your Aldena inbox and show you what an agent is waiting on you for.

## What's in it

- `.mcp.json` adds Aldena's remote MCP server, `aldena`, at `https://mcp.aldena.ai/mcp`. You sign in with OAuth, so the plugin holds no keys.
- The `agent-runs` skill tells Claude which Aldena tools to use for the inbox and for starting, following and stopping runs. When an agent asks a question or needs a tool approved, the skill has Claude show it to you and leave the choice to you.

## Install in Claude Code

In a Claude Code session, add the marketplace and install the plugin:

```text
/plugin marketplace add aldena-ai/integrations
/plugin install aldena@aldena
```

`/plugin install` opens the plugin's details, where you pick the scope to install it in. From a shell, run:

```bash
claude plugin marketplace add aldena-ai/integrations
claude plugin install aldena@aldena
```

Then run `/mcp`, pick `aldena` and sign in. Your browser opens Aldena's consent screen, where you choose Full access or Read-only. A Read-only connection gets only the tools that read. You need an Aldena account with a verified email.

## Install on claude.ai and in Cowork

Once the plugin is installed, the Aldena server shows on the plugin's Connectors tab under Customize > Plugins. Connect it there and sign in the same way. On a Team or Enterprise plan, an Owner adds the connector first.

## Use it

Ask in your own words, for example:

- "What's waiting on me in Aldena?"
- "Ask the agent in my web project to fix the flaky login test."
- "How is that run going?"
- "Stop the run in the api project."

Claude gives you the chat link for each run. When an agent asks a question or needs a tool approved, Claude shows it to you and sends back the answer you choose. You can also answer in the Inbox, at the link Claude shows you.

The server's other tools cover most of the app, from teams and projects to skills, routines and billing. Each one acts as you, with your role in each team. The [MCP server docs](https://docs.aldena.ai/mcp) list what stays in the app.

## Data

The plugin holds no code, so nothing from it runs on your machine. Claude keeps the sign-in token from your OAuth connection, and the plugin stores nothing. When Claude calls an Aldena tool, the call and its arguments go over HTTPS to `mcp.aldena.ai`, Aldena acts on your account, and the result comes back into your conversation. Aldena handles that data as its [privacy policy](https://aldena.ai/privacy) describes.

## Links

- Docs: https://docs.aldena.ai/mcp
- Privacy policy: https://aldena.ai/privacy
- Terms: https://aldena.ai/terms
- Support: support@aldena.ai

## License

MIT. See [LICENSE](LICENSE).
