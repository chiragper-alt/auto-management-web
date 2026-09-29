# Auto Management Web — Cloudflare Free API

This folder is an optional Cloudflare Workers + D1 backend. The web app remains local-first; this backend can be enabled later without changing the local `.amdb` workflow.

## Deploy
1. Install Wrangler: `npm install -g wrangler`
2. Login: `npx wrangler login`
3. Create D1: `npx wrangler d1 create auto-management-web`
4. Put the returned database id into `wrangler.toml`.
5. Apply schema: `npx wrangler d1 execute auto-management-web --remote --file=./schema.sql`
6. Set a strong secret: `npx wrangler secret put JWT_SECRET`
7. Deploy: `npx wrangler deploy`

## One Website / Three Roles
The same Worker URL can serve the web app and the API. The login screen has three roles:
- Developer — creates Dealer accounts and manages subscriptions/licenses.
- Dealer Admin — signs in with the Dealer ID and manages Operators.
- Operator — signs in with Dealer ID + Operator ID and receives only assigned permissions.

The included `site/index.html` is served by the Worker through the Assets binding, so no second website is required. The browser automatically uses the same origin as the API when deployed on `workers.dev`.

## API
- `GET /health`
- `POST /auth/developer-login` — `{loginId, password}`
- `POST /developer/bootstrap` — protected by `X-Bootstrap-Key`
- `GET /developer/dealers` — Developer JWT only
- `POST /developer/dealers` — Developer JWT only
- `PATCH /developer/dealers/status` — Developer JWT only
- `POST /auth/login` — `{dealerId, loginId, password}`
- `GET /me`
- `GET /operators`
- `PUT /operators`
- `PATCH /dealer`
- `GET /records`
- `POST /records/sync`

## Security
Use a specific production `ALLOWED_ORIGIN` instead of `*` after the web app has a stable domain. Passwords are never stored as plaintext; the worker stores salted SHA-256 hashes. Keep `JWT_SECRET` private.

## Provision the first Developer
Set a private bootstrap key with `npx wrangler secret put BOOTSTRAP_KEY`. From a one-time private provisioning script, POST developer id/name/password salt/hash to `/developer/bootstrap`. Do not expose this key in the browser.

## Provision a Dealer
After Developer login, use `POST /developer/dealers`. The browser Developer Panel does this automatically.

## Provision the first Dealer (legacy endpoint)
Set a private bootstrap key with `npx wrangler secret put BOOTSTRAP_KEY`. From your developer/admin tooling, POST the dealer id, admin id, dealer name, password salt/hash, plan and subscription fields to `/bootstrap` with header `X-Bootstrap-Key`. Do not expose this key in the browser.
