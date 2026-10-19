Auto Management Web v1.4.99 — Form 34 Generate + Preview Fix

Changes:
- Successful Generate Form 34 now opens the saved Form 34 Preview automatically.
- Generate button no longer restores stale button text after completion; saved/regenerate state is refreshed from storage.
- Generation errors remain visible through the existing notification path and are logged to the console.
- Added a clearer message if local document storage is blocked by another open app tab.

Validation:
- Inline JavaScript syntax checked with Node.js.
- ZIP archive integrity checked.
- Live browser workflow not executed in this environment.
