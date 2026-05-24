# Billing Webhooks

We send webhooks to your configured endpoint when billing events occur.

## Configuration

Configure your webhook endpoint in the Dashboard → Webhooks settings.

## Verification

Every webhook is signed with HMAC-SHA256. The signature is in the
`X-Webhook-Signature` header. Verify it against your webhook secret
to confirm the request came from us.

## Events

| Event | Description |
|-------|-------------|
| `invoice.created` | A new invoice has been created |
| `invoice.paid` | An invoice has been marked paid |
| `invoice.payment_failed` | A payment attempt failed |
| `subscription.created` | A new subscription started |
| `subscription.cancelled` | A subscription was cancelled |

## Payload format

```json
{
  "event": "invoice.paid",
  "timestamp": "2026-01-15T10:00:00Z",
  "data": { "id": "in_abc123", ... }
}
```
