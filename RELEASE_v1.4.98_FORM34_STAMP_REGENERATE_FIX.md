Auto Management Web v1.4.98 — Form 34 Financer Stamp & Regenerate Fix

- Financer Master remains the sole source of financer metadata and stamp image.
- Form 34 generation resolves financer by ID first, then normalized name, and has a direct local-storage fallback to the same `am_financers_v1` master key if the module API is not ready.
- Stamp must be a durable data:image/*;base64 URL or an HTTP(S) image URL. Blob URLs are rejected because they do not survive storage/reload.
- Stamp is positioned as an absolute overlay immediately above the “Signature of the financier” label.
- Generate/Regenerate button now has a busy state and refreshes saved status after generation.
- The uploaded Desktop v2.5.173 reference provides Form 34 layout/viewer, but its Financier Master code does not include a stamp-upload field or stamp lookup. This patch therefore uses the Web Financer Master source (`am_financers_v1`, `stampDataUrl`) rather than inventing a Desktop stamp mechanism.

Checks: ZIP integrity and inline JavaScript syntax checks. No live browser test performed.
