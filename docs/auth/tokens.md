# API Tokens

## Generating a token

1. Go to Dashboard → Developer → API Tokens
2. Click "Create new token"
3. Name your token (max 50 chars)
4. Select scopes
5. Click "Create"

The token is shown ONCE. Store it securely.

## Scopes

- `read` — read access to all resources
- `write` — create and update resources
- `admin` — manage tokens and team settings

## Token rotation

Tokens do not expire by default. Rotate every 90 days as a best practice.

## Revoking a token

Tokens can be revoked from the same Dashboard page. Revocation takes
effect within 60 seconds.
