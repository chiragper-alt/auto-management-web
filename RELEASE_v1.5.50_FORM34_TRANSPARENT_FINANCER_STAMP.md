# v1.5.50 — Form 34 Transparent Financer Stamp

- Financer stamp's near-white/white background is removed at Form 34 generation time using a client-side canvas.
- The original uploaded stamp in Financer Details remains unchanged; transparency is generated only for the Form 34 output.
- The generated transparent PNG is embedded in Form 34 so the page text behind/around the stamp is not covered by a white rectangle.
- If image decoding or canvas processing fails, the original stamp is used as a safe fallback.
- Existing Form 34 layout, A4 settings, stamp placement, and signature handling are unchanged.
