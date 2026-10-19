Auto Management Web v1.5.00 — Form 34 Generate / Preview Deep Fix

Base: user-provided Auto_Management_Web_v1.4.99_FORM34_GENERATE_PREVIEW_FIX.zip

Findings and changes:
1. Form 34 generation was hard-blocked when a matching Financer Master row had no usable stamp data URL. This prevented the document from being generated at all, which also meant the auto-preview path never ran. Stamp is now optional for generation: the document is generated without a stamp and a warning is logged; if a saved durable stamp exists it is still embedded.
2. IndexedDB open paths for saved-status and preview now safely create the `files` store during first-time database upgrade, and expose blocked/open errors instead of silently failing.
3. Preview failure is logged with a `[Form 34] Preview failed` console diagnostic; iframe is attached before its object URL is assigned.
4. Preserved customer/vehicle/financer data mapping, saved Form 34 key, and existing layout.

Validation:
- ZIP archive integrity checked.
- All 16 inline JavaScript blocks passed `node --check`.
- Full real-user browser workflow was not available for end-to-end validation; use the browser console if the issue persists.
