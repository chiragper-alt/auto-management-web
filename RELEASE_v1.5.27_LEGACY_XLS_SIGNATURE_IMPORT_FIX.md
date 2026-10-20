# Auto Management Web v1.5.27 — Legacy XLS Signature Import Fix

- Route spreadsheet imports using the actual file signature before relying on the filename extension. This supports legacy `.xls` uploads renamed by Android/file pickers to names such as `salesbilldata 1`.
- Validate that the legacy `.xls` reader returns a worksheet row array before passing it to the existing mapping/import pipeline.
- Preserve existing saved mappings, row validation, duplicate handling, and other application features.

Validation: tested the bundled legacy `.xls` parser against the supplied `salesbilldata 1` workbook; it returned 42 rows with the expected sales headers and data. ZIP integrity and JavaScript syntax checks are performed for the release. Browser end-to-end import has not been run in this environment.
