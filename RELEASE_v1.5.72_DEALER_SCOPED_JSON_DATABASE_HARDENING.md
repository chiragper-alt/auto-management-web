# Auto Management Web v1.5.73 — Dealer-Scoped JSON Database Hardening

- Upgraded exported database schema to v3 with stable database, admin, dealer and operator IDs.
- Exported operator records receive stable IDs when operator data exists in supported local storage keys.
- Database import validates the format/schema and dealer data section before applying it.
- Multi-dealer database imports require a matching active workspace rather than silently selecting the first dealer.
- Preserves existing browser data and legacy single-dealer JSON compatibility.
- JSON file remains local and requires the user to create/connect it through Settings → Data & Import.

Limitations: this is a local-first single-browser persistence layer, not a secure multi-user authentication system. Full dealer isolation across every module still requires all modules to use dealer-scoped repositories; browser localStorage alone is not a security boundary. No server/cloud sync is introduced.
