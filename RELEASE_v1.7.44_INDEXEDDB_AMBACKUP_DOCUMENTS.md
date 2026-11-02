# v1.7.44 — Complete IndexedDB + .ambackup Document Preservation

- Keeps every saved document binary in the existing local `AM_VAHAN_DOCUMENTS_V1` IndexedDB `files` store.
- Full Workspace `.ambackup` snapshots include every IndexedDB document binary as a Data URL, plus its record ID, document key, filename, MIME type and metadata.
- Backup creation now stops with an explicit error if any IndexedDB document row is missing its binary; it will not silently produce an incomplete backup.
- Restore validates the complete document section and every document entry before clearing/replacing the local document store.
- Restore writes the original document binaries back into IndexedDB and dispatches the document-changed event.
- Downloaded `.ambackup` files now update the displayed backup timestamp and document count.
- Preserves the Step 3 `Save` button and per-customer document persistence from v1.7.43.
- No Worker, D1, R2, authentication, subscription, dealer/operator isolation, or cloud document storage changes.

Validation: ZIP integrity and inline JavaScript syntax checks are performed. Full browser save/close/re-login/restore testing requires the deployed app and a real browser profile.
