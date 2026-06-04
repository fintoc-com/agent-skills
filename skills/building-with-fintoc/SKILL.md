---
name: building-with-fintoc
description: Provides context and best practices for building Fintoc integrations. Use when working with the Fintoc API, CLI, SDKs, or MCP servers — including writing integration code, debugging API errors, implementing payments or transfers, setting up webhooks, or exploring Fintoc documentation.
---

# Building with Fintoc

Fintoc is a Latin American fintech infrastructure API (Chile and Mexico). Four product areas:

- **Payments** — One-time and recurring bank payments. Chile and Mexico. → [payments.md](payments.md)
- **Transfers** — Programmatic payins/payouts. Chile ("Business Accounts") and Mexico (SPEI/CLABEs). → [transfers.md](transfers.md)
- **Movements** — Read-only bank transaction history via Links. Chile only ("Conexiones"). → [movements.md](movements.md)
- **Direct Debit** — Recurring charges via PAC (débito directo) on an authorized subscription. Chile only. → [direct-debit.md](direct-debit.md)

**Identify the product area and country before suggesting endpoints or flows.** If the use case or country isn't clear, ask first — the right product depends on both.

## Marketing name → product

Users arriving from fintoc.com may use marketing names. Map them to the right area:

| If the user mentions… | They need… | Area |
|---|---|---|
| "Smart Checkout", "checkout de pagos", "medios de pago" | Accept online payments | **Payments** |
| "Pagos Recurrentes", "suscripciones", "motor de cobro", "PAC", "PAC Digital" | Charge customers on a schedule | **Direct Debit** + recurring **Payments** |
| "Business Accounts" (Chile), "SPEI", "transferencias", "dispersar pagos", "recibir transferencias", "CLABEs" (Mexico) | Move money programmatically | **Transfers** |
| "Conexiones", "movimientos", "datos bancarios", "historial bancario", "link bancario" | Read a user's bank history | **Movements** |
| "Agents" | Not yet available via API — upcoming product with no docs yet. Let the user know. | — |

## How to use the docs

Docs are the source of truth. The reference files in this skill are **indexes only** — they route you to the right doc; they do not restate its contents.

- Append `.md` to any docs URL to read it as plain markdown (e.g. `https://docs.fintoc.com/docs/accept-a-payment.md`).
- Full machine-readable index: `https://docs.fintoc.com/llms.txt`
- **Always fetch the relevant doc before answering about a specific endpoint or flow** — don't answer from memory, as APIs change.

Per-area indexes: [payments.md](payments.md) · [transfers.md](transfers.md) · [movements.md](movements.md) · [direct-debit.md](direct-debit.md) · [webhooks.md](webhooks.md)

Cross-cutting concepts (auth, keys, pagination, idempotency, errors, metadata, common mistakes): [fundamentals.md](fundamentals.md)

## Tool selection

| Scenario | Tool |
|---|---|
| Server-side integration code | SDK or direct HTTP |
| Interactive API exploration | Fintoc CLI |
| AI agent making API calls | Fintoc API MCP (`mcp.fintoc.com`) |
| Answering docs questions in editor | Docs MCP (`docs.fintoc.com/mcp`) |
| Testing / triggering webhooks locally | Fintoc CLI |

Setup and details: [mcp-cli.md](mcp-cli.md)

## Where to get help

- Report unexpected MCP behavior using the `fintoc:feedback` tool.
- Email the Fintoc team at [product@fintoc.com](mailto:product@fintoc.com).
