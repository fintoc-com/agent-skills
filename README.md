# Fintoc Agent Skills

<img width="853" height="317" alt="image" src="https://github.com/user-attachments/assets/d5644446-1ab4-4c84-98c2-eb634ebf04a6" />

Agent skills for building with [Fintoc](https://fintoc.com), the financial infrastructure API for Latin America (Chile and Mexico). Built on the open [Agent Skills](https://agentskills.io) format.

## Installation

```bash
npx skills add fintoc-com/agent-skills
```

This installs the skills into your agent (Claude Code, Cursor, and other Agent Skills-compatible tools).

## Available skills

- **building-with-fintoc**: Context and best practices for building Fintoc integrations — the API, CLI, SDKs, and MCP servers. Covers Payments, Transfers, Movements, and Direct Debit, and routes you to the right documentation for each product and country.

## What are Agent Skills?

Agent Skills are folders of instructions and resources that agents discover and use to perform tasks more accurately. Each skill is a directory with a `SKILL.md` entrypoint and optional supporting files.

```
my-skill/
├── SKILL.md          # Required: instructions + metadata
└── references/       # Optional: supporting documentation
```

Skills use **progressive disclosure**: agents load only the name and description at startup, then read full instructions when a task matches. This keeps context usage efficient while giving agents detailed knowledge on demand.

## Working with the Fintoc API directly

The skills route you to Fintoc's documentation and tools. To let an agent call the API or search the docs, connect Fintoc's MCP servers:

| Server | URL | Use it for |
|--------|-----|------------|
| **API MCP** | `https://mcp.fintoc.com` | Letting an agent call the Fintoc API (OAuth on first connect; token scoped to `test` or `live`). |
| **Docs MCP** | `https://docs.fintoc.com/mcp` | Searching and retrieving documentation and code samples. |

You can also read any doc as plain markdown by appending `.md` to its URL (e.g. `https://docs.fintoc.com/docs/accept-a-payment.md`). The full machine-readable index is at `https://docs.fintoc.com/llms.txt`.

## Learn more

- [Fintoc documentation](https://docs.fintoc.com)
- [Building with AI (overview)](https://docs.fintoc.com/docs/building-with-ai.md)
- [Agent Skills specification](https://agentskills.io/specification)

## Help

- Report unexpected MCP behavior using the `fintoc:feedback` tool.
- Email the Fintoc team at [product@fintoc.com](mailto:product@fintoc.com).
