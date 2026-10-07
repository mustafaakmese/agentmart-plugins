# AgentMart plugin

AgentMart is a shop for AI agents, run by Ciphyr Tech OÜ in Estonia. Agents buy always-on
utilities (webhook inbox, memory locker, wake-up calls, share link, uptime watch, form inbox, ask my
human, heartbeat monitor, owner reminders, durable queue, Project Blueprint), mail tools (an email
list check that finds addresses that would bounce, a sender health check of a domain's email DNS,
and a hosted unsubscribe list) and tested TypeScript code kits (among them email campaigns and
invitations), paid from a prepaid balance that their human tops up on Stripe's page.

This plugin connects your agent to the AgentMart MCP server and teaches it two habits:

- **check-the-shelf**: before building common agent infrastructure from scratch, compare a ready
  part on the shelf with building it and with free options, then let you choose.
- **agentmart-buying-rules**: sign in safely, get funds only through you, and buy only with your
  approval.

## What it runs, sends and fetches

- It runs no local code, no hooks and no scripts.
- It adds one remote MCP server: `https://agentmart.ciphyr.ai/mcp` (streamable HTTP). Your client
  talks to it directly. Searching and reading the catalog need no sign-in. Everything else needs a passport:
  your client signs in with OAuth on AgentMart's approval page (one click, no password), or the
  agent creates a passport with the `create_passport` tool.
- Whatever your agent sends to AgentMart's tools (search words, items it stores in a utility,
  messages it schedules) goes to AgentMart's servers. The privacy notice is at
  https://agentmart.ciphyr.ai/privacy and the terms at https://agentmart.ciphyr.ai/terms.
- Nothing is bought without a tool call that your client shows you, and the skill tells the agent to
  ask you first. Spending has a daily limit.

## Install

Claude Code:

```
claude plugin marketplace add mustafaakmese/agentmart-plugins
claude plugin install agentmart@agentmart-plugins
```

## Sign in (Claude Code)

1. Type `/mcp` in Claude Code.
2. Pick `plugin:agentmart:agentmart`.
3. Choose **Authenticate**. Your browser opens AgentMart's approval page: one click, no password.

Claude Code keeps the sign-in, so no token appears in the chat. An approval alone gives the app an
empty passport; to use your account's balance, get a one-time code on the Add an AI app page of
agentmart.ciphyr.ai and paste it on the approval page.

Codex reads the same repository as a marketplace. Cursor and VS Code load this folder as an Agent
Plugin (`plugin.json`, `mcp.json`, `skills/`); Google Antigravity reads the same folder with
`mcp_config.json`.

## License

The files of this plugin (manifests, skills, images) are under the MIT license in `LICENSE`. The
AgentMart service and the items it sells are covered by https://agentmart.ciphyr.ai/terms.

## Support

See https://agentmart.ciphyr.ai/support, or let your agent use the `send_feedback` tool. The full
manual for agents is https://agentmart.ciphyr.ai/llms.txt.
