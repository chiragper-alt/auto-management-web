# Auto Management Web v1.5.69 — Form 34 Documents Record Context Fix

- Removed the strict dependency on opening Documents through a specific saved-documents entry point.
- Customer Details record view now records the active customer ID for the Documents workflow.
- Form 34 generation and signature save resolve the current customer ID from the active customer context when the saved-documents ID is not set.
- Documents button uses the active customer context as fallback.
- No customer data is reset or migrated.

Validation: source text patched; ZIP integrity to be checked. Browser runtime testing remains required.
