# Webhooks — index

Webhooks are the correct mechanism for asynchronous events (payment succeeded, transfer settled). **Do not poll for status.**

## Why it matters

- **Validate the signature on every request.** An unvalidated endpoint will happily process forged or replayed events.
- **Return 200 immediately, process in a background worker.** Slow handlers trigger retries and timeouts.
- **Deduplicate on event id and store the raw payload.** Fintoc may resend events; keeping the raw payload lets you replay safely.

The exact signing scheme, headers, and event names live in the docs — fetch them rather than hard-coding from memory.

## Docs

| Task | URL |
|---|---|
| Webhooks overview | `https://docs.fintoc.com/docs/webhooks-walkthrough.md` |
| Create webhook endpoint | `https://docs.fintoc.com/docs/webhooks-creating-guide.md` |
| Validate webhook signatures | `https://docs.fintoc.com/docs/webhooks-validating.md` |
| Test webhooks locally | `https://docs.fintoc.com/docs/webhooks-testing.md` |
| Webhook best practices | `https://docs.fintoc.com/docs/webhooks-good-practices.md` |
| Event types reference | `https://docs.fintoc.com/reference/types-of-events.md` |

Local testing/triggering is done with the Fintoc CLI — see [mcp-cli.md](mcp-cli.md).
