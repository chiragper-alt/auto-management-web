# Auto Management Web v1.5.63 — Extension API Blank Section Fix

- Fixed the Settings markup nesting bug that placed the Extension / API section inside the hidden Data & Import section.
- Extension / API is now a sibling settings section, so selecting its tab can display the API Key controls.
- Kept the existing Generate Key, Copy, local API-key storage, extension bridge, and chassis lookup logic unchanged.
- Removed no existing data or records. Browser/extension live testing is still required.
