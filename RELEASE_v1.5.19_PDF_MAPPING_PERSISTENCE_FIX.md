# Auto Management Web v1.5.19 — PDF Mapping Persistence Fix

- Persist invoice PDF mapping templates through the resilient storage layer and localStorage.
- Save selected PDF text positions for each mapped field.
- Build a more stable PDF layout key from common invoice labels instead of raw extracted invoice values.
- Reapply saved field coordinates on matching invoices so each new invoice supplies its own values rather than reusing old customer data.
- Existing pages and other features retained.

Validation: ZIP integrity and inline JavaScript syntax checks performed; live browser test not performed.
