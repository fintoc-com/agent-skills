# Fintoc MCP & CLI — index

Setup steps, config snippets, and the live tool/command lists live in the docs (they change often). This file only explains *which* tool to reach for and *why*.

## MCP servers

Fintoc has two MCP servers. Both work with Claude Code, Cursor, VS Code (MCP extension), and ChatGPT, and can run simultaneously.

| Server | URL | Use it for |
|---|---|---|
| **API MCP** | `https://mcp.fintoc.com` | Letting an AI agent call the Fintoc API. OAuth consent on first connect; a token is scoped to `test` **or** `live`, not both. |
| **Docs MCP** | `https://docs.fintoc.com/mcp` | Searching/retrieving documentation, code samples, and endpoint lookups without leaving the editor. |

The connected API MCP exposes its current tool set directly — list the available `fintoc:*` tools rather than relying on a hard-coded inventory, which drifts as tools are added or removed. Reference fully qualified names as `fintoc:<tool>` (e.g. `fintoc:fetch_resource`, `fintoc:list_payment_intents`).

**Safety:** enable human confirmation before tool execution, and be cautious combining this MCP with untrusted servers — prompt injection could trigger unintended API writes.

| Topic | URL |
|---|---|
| Building with AI (overview) | `https://docs.fintoc.com/docs/building-with-ai.md` |
| MCP server setup | `https://docs.fintoc.com/docs/model-context-protocol-mcp.md` |

## Fintoc CLI

Interactive API exploration and local webhook testing. Reach for it to make ad-hoc requests, forward webhooks to a local server (`fintoc listen`), or trigger test events (`fintoc trigger`).

| Topic | URL |
|---|---|
| CLI overview | `https://docs.fintoc.com/docs/cli.md` |
| Install the CLI | `https://docs.fintoc.com/docs/install-the-fintoc-cli.md` |
| Use the CLI | `https://docs.fintoc.com/docs/use-the-fintoc-cli.md` |
| Keys & permissions | `https://docs.fintoc.com/docs/fintoc-cli-keys-and-permissions.md` |
