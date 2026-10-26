# v1.5.71 — Local JSON Database Foundation

- Expanded the persistent `.json` / `.amdb` database file from master-record-only storage to include a snapshot of browser localStorage data/settings.
- Database file now carries schema version, local-first metadata, dealer identity, generated admin/dealer IDs, a dealer-scoped data container, and operator registry placeholder.
- Connect restores stored application settings/data and master records; subsequent localStorage writes are mirrored into the selected JSON database file while it remains connected.
- Existing local browser storage remains in place; no records are intentionally cleared.

## Important scope
This is a local single-browser database/persistence foundation, not a completed secure multi-tenant authorization system. Current application modules still use shared browser storage and are not all isolated by dealer at runtime. True dealer-wise access isolation requires scoping each module's reads/writes by dealer ID and authenticated admin/operator identity, plus migration and regression tests. The JSON file contains sensitive business/customer data and should be stored securely with backups.
