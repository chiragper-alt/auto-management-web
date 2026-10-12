# Import Center rebuild notes

Base: Auto Management Web v1.4.33 Import Section Clean Rebuild.

Implemented in this update:
- Excel/CSV import routes `.xls` through the existing legacy BIFF parser, `.xlsx` and `.xlsm` through the offline workbook parser, and CSV through the CSV parser.
- Import errors are surfaced in the Import Center rather than silently ignored.
- Prevented nested upload buttons from double-triggering the label/file input click.
- PDF extraction patterns include the sample Century Bikes invoice's `To,` customer block, `M :` mobile label, `Invoice Dt.`, `TOTAL AMOUNT`, `MODEL`, and `COLOUR` labels.
- Saved PDF template values fill only fields that the current extraction did not find.

Known limitations:
- Scanned/image-only PDFs still require OCR; the current extraction uses selectable PDF text.
- `.xlsb` is not supported.
- Browser end-to-end testing against the user's exact browser is still required.
