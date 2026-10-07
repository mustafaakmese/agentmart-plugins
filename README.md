# AgentMart plugins

Plugins that connect your AI agent to [AgentMart](https://agentmart.ciphyr.ai), a shop where agents use always-on
utilities (webhook inbox, memory locker, wake-up calls, uptime watch, bounce check, sender health check, unsubscribe
list and more) and download tested code kits, paid from a prepaid balance that their human tops up.

Made by Ciphyr Tech OÜ, the company behind AgentMart. Contact: support@ciphyr.ai.

## What the plugin adds

- The AgentMart MCP server (`https://agentmart.ciphyr.ai/mcp`). You sign in once through your app's own sign-in:
  one approval click in the browser, no password, and no token in the chat.
- Two skills:
  - **check-the-shelf**: before building common agent infrastructure from scratch, compare a ready AgentMart part
    with building it yourself and with free options, then ask your human. It says when not to use AgentMart.
  - **agentmart-buying-rules**: buy only with your human's clear yes; never spend without it.

Nothing here costs money by itself. Prices are read live from the shop, so this repository never shows a stale price.

## Install

**Claude Code**

```
claude plugin marketplace add mustafaakmese/agentmart-plugins
claude plugin install agentmart@agentmart-plugins
```

Then sign in once: type `/mcp`, pick `plugin:agentmart:agentmart`, choose **Authenticate**.

**Codex**: `codex plugin marketplace add mustafaakmese/agentmart-plugins`, then install it from the Plugins Directory.

**Cursor**: copy `plugins/agentmart` to `~/.cursor/plugins/local/agentmart`.

**VS Code**: run "Chat: Install Plugin From Source" with this repository's address.

**Gemini CLI (company plans) and Antigravity**: this repository is also a Gemini extension
(`gemini-extension.json` at the root). Antigravity reads `plugins/agentmart/mcp_config.json`.

**Any other MCP client**: add the server `https://agentmart.ciphyr.ai/mcp` (streamable HTTP, OAuth).

## Links

- Shop: https://agentmart.ciphyr.ai/shop
- For agents: https://agentmart.ciphyr.ai/llms.txt
- Terms: https://agentmart.ciphyr.ai/terms and privacy: https://agentmart.ciphyr.ai/privacy

## License

The files in this repository are MIT licensed (see LICENSE). AgentMart itself is a paid service with its own terms.
