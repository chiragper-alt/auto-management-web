# v1.5.70 — Admin Profile, Dealer Workspace, Sign out

- Replaced placeholder admin-menu notifications with functional Profile and Dealer Workspace dialogs.
- Profile saves display name, email, mobile and language preference in browser-local settings.
- Dealer Workspace saves company name, dealer/RTO code, address, business contacts and optional logo URL locally.
- Saved profile display name is reflected in the top-right admin menu.
- Sign out now asks for confirmation and explicitly preserves local customer/vehicle data. This build has no authentication/session backend, so it does not claim to revoke a real login session.
- Existing application data and modules are retained.

Validation: ZIP integrity and inline JavaScript syntax checks required before release; browser end-to-end testing remains necessary.
