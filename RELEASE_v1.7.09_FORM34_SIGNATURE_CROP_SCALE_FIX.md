# v1.7.09 — Form 34 Signature Crop and Scale Fix

- Generated transparent signature PNG is cropped to visible ink bounds with small transparent padding.
- Removes large transparent canvas margins that previously caused the actual signature to print tiny.
- Form 34 owner signature display increased to max 72×22 mm.
- Signature area expanded to 25 mm to prevent label collision.
- Existing signatures must be regenerated and saved once to benefit from tight cropping.
- No Auth Worker or D1 changes.
