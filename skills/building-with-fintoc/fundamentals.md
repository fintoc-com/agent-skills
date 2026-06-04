# API Fundamentals — index

Cross-cutting concepts that apply across all product areas. Each entry explains *why it matters*; the exact headers, defaults, and enum values live in the linked doc — fetch it before relying on specifics.

## Authentication & keys

The secret key goes directly in the `Authorization` header (no encoding, no basic-auth password). Key types:

- `sk_live_` / `sk_test_` — server-side only, **never** in frontend or browser code.
- `pk_live_` / `pk_test_` — safe for the web checkout / browser.

Test keys hit the same API with simulated bank responses. Always develop against test mode.

| Topic | URL |
|---|---|
| API keys | `https://docs.fintoc.com/docs/api-keys.md` |
| Test mode | `https://docs.fintoc.com/docs/test-mode.md` |

## Pagination

Navigation is via the response `Link` header, not a body field, and the scheme differs between API versions — don't assume one style works everywhere. A naive single-page fetch silently drops records. The Python and Node SDKs paginate automatically.

→ `https://docs.fintoc.com/reference/pagination.md`

## Idempotency

Send an idempotency key (use your internal order ID) on payment/transfer creation so a retried request doesn't double-charge. Treat this as required in production.

→ `https://docs.fintoc.com/reference/idempotent-requests.md`

## Errors

Branch on the error *type*, not the message: bad-parameter errors should not be retried, rate-limit errors need exponential backoff, and Fintoc-side errors are safe to retry.

→ `https://docs.fintoc.com/reference/errors-object.md`

## Metadata

Attach your own IDs and references to objects so you can reconcile against your system without a separate lookup table.

→ `https://docs.fintoc.com/reference/metadata.md`

## Rate limits

→ `https://docs.fintoc.com/docs/api-rate-limits.md`

## SDKs

→ `https://docs.fintoc.com/docs/libraries-and-integrations.md`

## Common mistakes

- Live keys in dev/staging.
- No idempotency key on payment/transfer creation → duplicate charges on retry.
- Polling for status instead of using webhooks (see [webhooks.md](webhooks.md)).
- `sk_` key in frontend code.
- Single-page list fetch without pagination → silently missing records.
- Skipping webhook signature validation.
- Outbound transfers without JWS setup → rejected immediately (see [transfers.md](transfers.md)).
