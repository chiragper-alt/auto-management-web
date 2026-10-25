# v1.5.73 — Local Database Isolation & Backup Fix

- One JSON database file is explicitly scoped to one dealer workspace.
- Database schema v4 includes Admin, Dealer, and Operator IDs and dealer-tagged records.
- Database open validates the file format, dealer identity, record scope, and JSON integrity before restoring.
- Prevents a mismatched dealer database from silently overwriting the current workspace.
- Uses a dealer-specific suggested filename and preserves the existing local-first architecture.
- Browser storage remains the app runtime store; the selected JSON file is the persistent mirror while connected.
- Authentication/session security and a full migration of every module to independent per-dealer storage remain separate work and are not claimed as complete.
