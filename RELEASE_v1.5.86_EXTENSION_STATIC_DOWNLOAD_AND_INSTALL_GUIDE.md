# Release v1.5.86 — Extension static download and install guide

- Added a static ZIP download link to Settings → VAHAN Extension / API.
- Added collapsible Chrome/Chromium install and update instructions.
- Audited the supplied extension ZIP: Manifest V3; required background, popup, bridge and content-script files are present.
- Version audit finding: uploaded ZIP filename says v1.3.22, but `VAHAN_Extension/manifest.json` declares version `1.3.21`. To avoid misrepresenting the package, the website download is named v1.3.21 and the UI explicitly notes the mismatch.
- This release does not upgrade the extension code or change its manifest version.
