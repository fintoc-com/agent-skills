# Transfers — index (Chile and Mexico)

Programmatic payins/payouts. Marketed as "Business Accounts" in Chile and via SPEI/CLABEs in Mexico.

## Non-obvious behaviors

- **Outbound transfers require one-time JWS key setup** before the first payout, in both Chile and Mexico. Without it, payouts are rejected immediately. Do this before building the payout flow.
- **In Mexico, verify a CLABE before sending** to avoid failed or misrouted payouts.

See [fundamentals.md](fundamentals.md) for idempotency (avoid duplicate payouts on retry) and error handling.

## Docs

| Task | URL |
|---|---|
| Transfers overview | `https://docs.fintoc.com/docs/transfers-overview.md` |
| Transfers quickstart | `https://docs.fintoc.com/docs/transfers-quickstart.md` |
| Pick your use case | `https://docs.fintoc.com/docs/transfers-use-cases.md` |
| Receive transfers (payins) | `https://docs.fintoc.com/docs/inbound-transfers.md` |
| Send transfers (payouts) | `https://docs.fintoc.com/docs/outbound-transfers.md` |
| Batch transfers | `https://docs.fintoc.com/docs/batch-transfers.md` |
| Return an inbound transfer | `https://docs.fintoc.com/docs/returning-an-inbound-transfer.md` |
| Account statements | `https://docs.fintoc.com/docs/account-statements.md` |
| Test transfers | `https://docs.fintoc.com/docs/test-your-integration.md` |
| Generate JWS keys (required for outbound) | `https://docs.fintoc.com/docs/setting-up-jws-keys.md` |
| Security controls | `https://docs.fintoc.com/docs/security-controls.md` |

### Use-case guides

| Use case | URL |
|---|---|
| Payins on dedicated account numbers | `https://docs.fintoc.com/docs/collect-payments-with-dedicated-account-numbers.md` |
| Payouts to users or suppliers | `https://docs.fintoc.com/docs/send-payouts-to-users-or-suppliers.md` |
| Wallet for end users | `https://docs.fintoc.com/docs/run-a-wallet-for-end-users.md` |
| Payroll or bulk payouts | `https://docs.fintoc.com/docs/run-payroll-or-bulk-payouts.md` |
| Verify a CLABE before payout | `https://docs.fintoc.com/docs/verify-a-clabe-before-paying-out.md` |

### CLABE / Account Numbers (Mexico)

| Task | URL |
|---|---|
| Disable account numbers and set transfer limits | `https://docs.fintoc.com/docs/add-logic-to-clabes.md` |
| Manage account number usage | `https://docs.fintoc.com/docs/manage-your-clabes.md` |
| Verify a CLABE before payout | `https://docs.fintoc.com/docs/verify-clabes.md` |
