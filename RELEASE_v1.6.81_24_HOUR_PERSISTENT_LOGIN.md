# v1.6.81 — 24-Hour Persistent Login

- Extended successful login session expiry from 8 hours to 24 hours.
- Persisted the authenticated session in localStorage so closing and reopening the browser does not immediately require signing in again.
- Session restore checks the stored expiry timestamp and automatically clears expired sessions.
- Logout still clears the persistent session immediately.
- Dealer/Operator active-status checks and existing role/page permissions remain in place.
- Existing valid sessionStorage sessions are migrated to persistent localStorage on restore.

Validation: ZIP integrity and inline JavaScript syntax checked. Browser restart/login test not performed.
