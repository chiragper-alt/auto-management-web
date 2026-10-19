# Auto Management Web v1.5.18 — Global Page Isolation Fix

- Resets inline `!important` display/visibility/opacity/pointer-events styles used by Customer / Vehicle Record view whenever navigation changes.
- Clears stale page-content markup when returning to Dashboard.
- Replaces previous page content before rendering another menu, preventing edit screens and mapping previews from remaining mounted across pages.
- Preserves the existing data-save behavior and other features.

Validation: ZIP integrity and JavaScript syntax checks; live-browser functional testing remains pending.
