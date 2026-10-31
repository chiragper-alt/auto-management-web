# v1.7.05 — Exact Font Rendering, No Language Conversion

- Removed English-to-Gujarati transliteration UI and conversion logic entirely.
- Input is rendered exactly as typed, in the selected uploaded/system font.
- Gujarati text remains Gujarati; English text remains English.
- Preview and PNG export continue to use the selected font.
- No Auth Worker or D1 changes.
- Note: selected font must contain glyphs for the entered script; otherwise browser fallback applies.
