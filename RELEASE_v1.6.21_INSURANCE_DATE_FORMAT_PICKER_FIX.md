# v1.6.21 - Insurance date format and picker fix

- Policy dates normalize to DD-MM-YYYY in the PDF import mapping, without OCR time/text suffixes.
- Imported dates save in YYYY-MM-DD for HTML date-input compatibility.
- Customer record date rendering accepts date strings with trailing OCR text.
- Existing insurance dropdown and import workflow retained.

ZIP integrity checked; browser end-to-end import not tested in this environment.
