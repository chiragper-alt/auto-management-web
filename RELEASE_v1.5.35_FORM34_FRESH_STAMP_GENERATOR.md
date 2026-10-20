# Auto Management Web v1.5.35 — Fresh Form 34 Stamp Generator
- Rebuilt Form 34 generation independently in the Documents UI script; no legacy Form 34 generation/preview/stamp lookup code reused.
- Resolves the active customer record from the saved-documents context and matches Financer Master by ID first, then normalized name.
- Reads saved stampDataUrl from am_financers_v1 and embeds it directly in the generated printable Form 34 page at the “Signature of the financier” position.
- Preserves the two specimen-signature spaces at the bottom.
- Adds explicit status when no customer record, popup access, or saved financer stamp is available.
- Uses browser Print / Save as PDF for output. Live browser testing remains required.
