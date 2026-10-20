# Auto Management Web v1.5.33 — Excel Import Clean Rebuild

- Removed the legacy Excel/CSV parser implementations (`AMXLS`, `AMXLSX`).
- Removed the old Excel/CSV import pipeline, column definitions, auto-mapping, mapping modal, saved mapping controller, row matching/update-from-mapping logic, and `processExcel` handler.
- Removed Settings > Data & Import legacy Mapping Settings UI and its controller. Persistent database file controls remain.
- Kept the Excel/CSV tab and upload area as UI-only placeholder for a future fresh implementation.
- Kept the PDF invoice import implementation and PDF saved-template mapping path untouched by this cleanup.
- One-time startup cleanup removes obsolete `am_import_mappings_v2` and `am_import_settings_v1` local-storage keys so the new implementation does not inherit legacy Excel mapping state. Other records/settings are not cleared.

Checks performed:
- All 14 inline script blocks passed `node --check`.
- Grep audit found no remaining legacy Excel import/mapping functions or parser globals in application source.
- ZIP integrity checked after packaging.
- Browser live test not performed in this environment.
