Auto Management Web v1.6.27 — Customer Document Isolation Fix

Based on v1.6.26. Fixes document thumbnails/assignments leaking across customer views by clearing saved-document UI state before loading a different customer. Saved files are loaded only when both recordId and the customer-scoped key match the active record. Import-created invoice and insurance files remain keyed by customer record ID.

Validation: ZIP integrity checked. Browser end-to-end testing not performed.
