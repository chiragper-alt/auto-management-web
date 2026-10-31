# Auto Management Web v1.7.02 — Gujarati Signature Font & Live Typing

## Signature Generator updates
- Added local Gujarati font upload for TTF, OTF, WOFF and WOFF2 files.
- Uploaded font binaries are stored in a separate browser IndexedDB database (`AM_SIGNATURE_FONTS_V1`); no D1/Auth Worker changes are required.
- Added a font selector and preview; uploaded fonts can be selected again in the same browser profile.
- Added live English-to-Gujarati phonetic transliteration in the generated-signature input.
- Generated PNG signature uses the selected Gujarati font and Gujarati-transliterated text.
- Existing Draw Sign, customer-local document save, and Form 34 signature retrieval paths are preserved.

## Notes / limitations
- This is an offline lightweight transliteration implementation with common-name overrides; it is not a full Indic transliteration engine. Proper nouns and ambiguous spellings should be reviewed in the preview before saving.
- Font files are browser-local, not Windows system-installed and not automatically synchronized to another computer/browser profile.
- The default font stack uses Noto Sans Gujarati / Shruti where available. Upload a Unicode Gujarati font for consistent rendering.
- UI and signature generation only; no Auth Worker or D1 migration is required.
