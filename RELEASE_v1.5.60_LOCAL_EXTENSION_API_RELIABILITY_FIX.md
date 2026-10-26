# v1.5.60 — Local Extension/API Reliability Fix

- Fixed Extension popup Connect verification to call the direct authenticated API-key verifier used by the background service worker.
- A failed verification now shows an error and does not claim the extension is connected or save an invalid key.
- Chassis lookup remains on the direct bridge and reads the Auto Management Web tab's local master-record store.
- Tab selection now requires the page title to identify Auto Management, preventing the extension from selecting an unrelated browser tab.
- No cloud backend is required for same-computer use; keep Auto Management Web open in the same Chrome profile.
- For a local HTML file, enable the extension's “Allow access to file URLs” permission and reload the extension and app tab.

## Validation
- JavaScript syntax checks passed for popup.js, background.js and web-bridge.js.
- manifest.json parsed successfully.
- Full Chrome + VAHAN live interaction testing still needs to be performed on the user's computer.
