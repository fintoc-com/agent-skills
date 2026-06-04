# Payments — index (Chile and Mexico)

One-time and recurring bank payments. The web checkout authenticates the user's bank. Core API objects: Checkout Sessions, Payment Intents, Payment Methods, Customers. (Some existing integrations use the Widget — supported but no longer actively sold; see [webhooks.md](webhooks.md) and the Widget docs below.)

Recurring charges in Chile are often implemented with **Direct Debit (PAC)** — see [direct-debit.md](direct-debit.md).

Read [fundamentals.md](fundamentals.md) for auth, idempotency, and error handling before writing payment-creation code.

## Docs

| Task | URL |
|---|---|
| Payments quickstart | `https://docs.fintoc.com/docs/quickstart-payments.md` |
| Payment scenarios overview | `https://docs.fintoc.com/docs/payments-use-cases.md` |
| Accept a one-time payment | `https://docs.fintoc.com/docs/accept-a-payment.md` |
| Accept recurring payments | `https://docs.fintoc.com/docs/accept-recurring-payments.md` |
| Save a payment method for future use | `https://docs.fintoc.com/docs/save-a-paymentmethod-of-a-customer-for-future-payments.md` |
| Check payment eligibility | `https://docs.fintoc.com/docs/check-payment-eligibility.md` |
| Handle payment exceptions | `https://docs.fintoc.com/docs/dealing-with-payment-exceptions.md` |
| Refund a payment | `https://docs.fintoc.com/docs/payment-initiation-refunds.md` |
| Test payments | `https://docs.fintoc.com/docs/payment-initiation-test-your-integration.md` |
| Go-live checklist | `https://docs.fintoc.com/docs/go-live-checklist.md` |

### Widget (legacy)

| Topic | URL |
|---|---|
| Widget overview | `https://docs.fintoc.com/docs/widget.md` |
| Web integration | `https://docs.fintoc.com/docs/web-integration.md` |
| WebView integration | `https://docs.fintoc.com/docs/webview.md` |
| Widget events | `https://docs.fintoc.com/docs/widget-events.md` |
