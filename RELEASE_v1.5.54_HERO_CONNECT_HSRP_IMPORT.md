# v1.5.54 — Hero Connect HSRP Import & Record

## Changes
- Replaced Hero Connect placeholder panels with a dedicated two-file import and HSRP Record workspace.
- Added HSRP Order and SalesBillData file selection, parsing, preview, exact normalized chassis matching, and explicit import confirmation.
- Retains every HSRP source row, including rows without a SalesBillData match.
- Registration Number and Registration Date are taken only from HSRP Order Excel.
- `Order Dealer Name` is intentionally ignored and is not used as a record field.
- Adds matched, sales-bill-missing and review status counts, searchable/filterable records, and CSV export.
- Hero Connect styles are scoped to `#hero-connect-ui`; module logic is isolated in `am-hero-connect-module`.
- Imported records are stored in browser localStorage under `am_hero_connect_hsrp_records_v1`, separate from other module records.

## Notes
- XLS/XLSX parsing loads SheetJS from jsDelivr when needed, so the first import requires internet access unless SheetJS is already available in the page.
- Matching is exact after uppercasing and removing whitespace; no fuzzy matching is performed.
- If multiple sales rows match a chassis, the record is flagged for review and bill fields are left blank rather than silently choosing one.
