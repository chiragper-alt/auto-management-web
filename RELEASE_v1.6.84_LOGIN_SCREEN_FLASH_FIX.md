# v1.6.84 — Login Screen First-Paint Flash Fix

- Root cause: the full dashboard/app shell was rendered visibly by the browser before the bottom-of-page authentication script restored the session and created the login overlay.
- Added a tiny early `<head>` CSS guard that hides `.app-shell` until authentication is resolved.
- Valid restored session: `activate()` reveals the application shell.
- No valid session: login gate is shown while the application shell remains hidden.
- Logout hides the application shell before returning to Dealer Login.
- This changes only initial visibility/auth presentation; existing login credentials, roles, permissions, and data modules are preserved.

Validation: inline JavaScript syntax and ZIP integrity checked. Browser hard-refresh verification is still required.
