# Auto Management Web v1.5.61 — Extension API Tab Only Fix

- Removed the duplicate top-right “Extension / API Key” button from Settings.
- Kept the existing Settings → Extension / API tab as the single place for API key generation, copy, and status.
- Preserved the existing local API key storage and extension/chassis lookup bridge code.
- Version update only; no API key is generated automatically and existing keys are not reset.

Validation: ZIP integrity and embedded JavaScript syntax checks should be run before release; live Chrome-extension pairing still requires testing on the target computer.
