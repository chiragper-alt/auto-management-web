# v1.6.85 — Extension Version Checker

- Added Installed Version detection through the connected Chrome extension bridge.
- Added Latest Version lookup from the Cloudflare `version.json` release manifest.
- Added Update Available / latest-version status and manual Check for Updates action.
- Extension download URL and filename are populated from the release manifest.
- Base: Auto Management Web v1.6.84.
- Fixed Settings-page JavaScript source leak: moved the Version Checker script out of the Form 34 HTML template literal and placed it after the application markup.
- Preserved the existing Form 34 generation, preview, save, and Document Viewer logic.

