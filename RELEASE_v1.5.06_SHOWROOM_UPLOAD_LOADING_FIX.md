# Auto Management Web v1.5.06 — Showroom Photo / Loading Fix

- Compress showroom photos client-side to a max 1600px edge and JPEG quality 0.82 before saving to browser storage, reducing localStorage quota failures.
- Increase accepted source image limit to 12 MB, while saving an optimized copy.
- Verify saved branding data and provide a useful error if browser storage cannot persist it.
- Ensure the global page-loading overlay is dismissed if page rendering fails, including a failed retry.
- Keep existing dealer-specific branding keys and default-image fallback.

Validation: ZIP integrity and inline JavaScript syntax checks performed. Browser live test remains required.
