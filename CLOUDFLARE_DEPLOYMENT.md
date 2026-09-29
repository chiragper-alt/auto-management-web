# Auto Management Web — Optional Cloudflare Mode

Version 1.5.2 keeps the existing **local-first** workflow and adds an optional Cloudflare Workers + D1 mode.

## What is included
- `cloudflare/worker.js` — API for login, dealer profile, operators and record sync.
- `cloudflare/schema.sql` — D1 schema.
- `cloudflare/wrangler.toml` — Wrangler configuration template.
- `cloudflare/README.md` — deployment and security instructions.
- `index.html` — Cloudflare settings panel and optional cloud login/sync bridge.

## Local-first behavior
Cloud mode is **OFF by default**. Existing `.amdb` local database and browser-local operation continue to work without any server.

When Cloudflare mode is enabled and an API endpoint is configured:
- Dealer Admin/Operator login can authenticate against the Worker.
- Dealer profile and Operator metadata can sync.
- Master Records can sync to D1.
- Local `.amdb` remains available as a backup/offline workspace.

## Production setup
1. Create a Cloudflare account and install Wrangler.
2. Create a D1 database and put its ID in `cloudflare/wrangler.toml`.
3. Run the included `schema.sql` against the remote D1 database.
4. Set `JWT_SECRET` with `wrangler secret put JWT_SECRET`.
5. Set `BOOTSTRAP_KEY` with `wrangler secret put BOOTSTRAP_KEY`.
6. Deploy the Worker.
7. Provision each Dealer through the private `/bootstrap` endpoint from your developer/admin tooling. Never expose `BOOTSTRAP_KEY` in the web app.
8. In Auto Management Web → Settings → Cloudflare, enter the Worker URL, test the connection, then enable Cloud Mode.

## Important
The bundled API is a deployment-ready foundation, not a server that has already been deployed. No Cloudflare account or credentials are included in the ZIP.


## Single-site deployment
This package now serves both the Auto Management Web UI and API from the same Cloudflare Worker URL. The login page is role-based: Developer, Dealer Admin, and Operator. The Worker uses the `site/` assets binding; `/health`, `/auth/*`, `/developer/*`, `/operators`, `/dealer`, and `/records/*` remain API routes.

After deploying, the same `https://<worker-name>.<subdomain>.workers.dev` URL is the only URL you give users. Developer creates Dealers; Dealer Admin creates Operators.
