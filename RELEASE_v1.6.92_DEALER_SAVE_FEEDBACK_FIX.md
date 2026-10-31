# v1.6.92 — Dealer Save Feedback Fix

Base: v1.6.91_DOCUMENT_SECTION_UI_POLISH

Changes:
- Dealer Save button now visibly switches to Saving Dealer… / Updating…
- Displays server response and API errors in a prominent inline status area.
- Restores button state after success or failure.
- Logs detailed failures to browser console for diagnosis.
- Aligns password minlength UI validation with the server minimum of 8 characters.
- Removes the unsupported Custom plan option from the current Dealer form; Basic, Standard and Premium are supported by seeded plans.
- Does not change customer records/documents or their local storage.
- Does not change Worker code or D1 schema.
