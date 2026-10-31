# Auto Management Web v1.7.03 — Documents Page Fix

## Critical fix
- Fixed a JavaScript syntax error in the Gujarati Signature Font loader introduced in v1.7.02.
- The font loader used `await` inside a non-async callback, which prevented the containing application script from parsing and stopped the Documents route from rendering.
- Changed the font restoration callback to an async callback and await font loading correctly.

## Preserved
- v1.7.02 Gujarati font upload and live transliteration feature.
- v1.7.01 sidebar and flat document thumbnail UI changes.
- Existing Documents, Master Records, signature save and other workflows.
- No Auth Worker or D1 changes required.

## Validation
- All 25 inline JavaScript blocks pass `node --check`.
- ZIP integrity check performed after packaging.
