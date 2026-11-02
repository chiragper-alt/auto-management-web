# v1.7.41 — Form 34 Signature & Stamp Alignment

- Based on v1.7.40.
- Moved the owner signature image upward by 18 PDF-render coordinate units; the owner signature label remains unchanged.
- Moved the already-reduced financier stamp farther left by 35 units and lower by 33 units.
- Kept stamp dimensions at 232 × 142 render units (the approximately 3 mm reduction from v1.7.40).
- Direct PDF generation and IndexedDB storage are unchanged.

Validation:
- ZIP integrity verified.
- Source patch assertions passed.
- Full browser PDF preview and physical print alignment have not been tested in this environment. Please generate a fresh Form 34 PDF to verify the final placement.
