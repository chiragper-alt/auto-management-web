# v1.6.26 — Insurance Date Picker Import Fix

- Based on v1.6.25; preserves the existing UI and full insurer names.
- Normalizes imported/mapped policy dates to ISO `YYYY-MM-DD`, the value format required by HTML date-picker inputs.
- Supports numeric dates and common month-name date formats, and rejects invalid calendar dates.
- ZIP integrity validated; browser end-to-end testing was not available in this build environment.
