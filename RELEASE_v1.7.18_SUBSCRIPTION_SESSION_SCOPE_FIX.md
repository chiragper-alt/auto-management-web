# v1.7.18 — My Subscription Session Scope Fix

- Fixed My Subscription referencing `session` and `SESSION_KEY` from a different JavaScript closure.
- Reads the active auth session through the existing `window.__amAuthGetSession()` accessor.
- Updates the existing sessionStorage subscription snapshot only when the stored auth token matches the active token.
- Removed the out-of-scope `allowed()` navigation refresh from this module.
- Improved API-load error handling so the plan selector no longer remains on a misleading Loading state after failure.
- Based on v1.7.17; retains document thumbnail, Add Files tile, Form 34, and signature changes.
- Worker API was not modified.
