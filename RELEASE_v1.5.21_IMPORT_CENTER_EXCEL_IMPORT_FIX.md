# Auto Management Web v1.5.21 — Import Center Excel Import Fix

- Improved XLSX worksheet relationship path normalization for workbooks that store relative, absolute, or parent-relative worksheet targets.
- Improved Import Center feedback to show per-file errors, row-level validation examples, and a combined import summary instead of overwriting errors with a generic message.
- Preserved existing Excel/CSV column mapping and required Owner Name / Chassis No. validation.

Validation: ZIP integrity checked; all 15 inline JavaScript blocks pass `node --check`. Live browser testing has not been performed.


## v1.6.53 — Customer-field-based Excel mapping
- Mapping destinations are stable Customer Details fields; Excel column names are only source choices.
- Added address, landmark, city/town, district, state, pincode, mobile, HPA, purchase date and bill fields.
- Excel header aliases are used only for Auto-map suggestions and can vary by dealer format.
