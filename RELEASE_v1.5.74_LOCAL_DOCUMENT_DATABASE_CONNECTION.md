# Auto Management Web v1.5.74 — Local Document Database Connection

## Changes
- Connected the persistent dealer JSON database snapshot to the existing local IndexedDB document store (`AM_VAHAN_DOCUMENTS_V1`).
- JSON database sync now includes local document metadata and file contents (serialized as data URLs) under the active dealer scope.
- Connecting/restoring a dealer database restores its documents into IndexedDB and emits `am-document-changed` so document UI can refresh.
- Document entries are validated before restore; entries without keys or record IDs are rejected.
- Existing local document storage remains local to the browser unless the user explicitly exports/connects the dealer JSON database file.

## Notes
- Local browser persistence uses IndexedDB for binary files; localStorage is not suitable for large PDFs/images due to quota limits. The connected JSON database file provides an explicit portable snapshot/sync target.
- Browser File System Access requires a supported Chromium browser and granted file permission.
- Validate document upload, Form 34 save/view, JSON export, and restore in the target browser before production use.
