# Invoices API

## List invoices

`GET /v1/invoices`

Returns a paginated list of invoices for the authenticated account.

### Query parameters

- `limit` (integer, default 50, max 100)
- `starting_after` (string) — cursor for pagination
- `status` (string) — filter by status: `draft`, `open`, `paid`, `void`

### Response

```json
{
  "data": [
    {
      "id": "in_abc123",
      "amount_cents": 1500,
      "currency": "usd",
      "status": "paid",
      "created_at": "2026-01-15T10:00:00Z"
    }
  ],
  "has_more": false
}
```

## Get invoice

`GET /v1/invoices/{id}`

Returns a single invoice by ID.
