# v1.7.39 — Form 34 Direct PDF Generation

- Replaced Form 34 HTML-file generation/storage with direct PDF byte generation in the browser.
- Uses the built-in Canvas/SVG rendering path and an embedded PDF 1.4 writer; no CDN, network request, print dialog, or HTML-to-PDF conversion is required.
- Generated PDF is stored locally in the existing `AM_VAHAN_DOCUMENTS_V1` IndexedDB `files` store under the existing `recordId:form34` key.
- Document metadata now records `application/pdf`; the existing Document Viewer opens the saved PDF, and Download saves the `.pdf` file directly.
- Preserves the Form 34 fields, A4 portrait page, title/subtitle/body typography intent, owner signature and transparent Financer stamp.
- PDF page is rasterized at 300 dpi to preserve browser-rendered glyphs and embedded signature/stamp appearance. Text in the resulting PDF is therefore not selectable/searchable.
- Older saved HTML Form 34 documents remain in local storage; users should generate Form 34 again to replace the old item with a PDF.
- Existing generic document upload/PDF handling was not modified.

Validation:
- All inline JavaScript blocks passed `node --check`.
- Direct PDF writer produced a valid one-page A4 PDF in a Node test harness; `pdfinfo` and `pdftoppm` successfully parsed/rendered the test PDF.
- Full browser UI, real customer data, signature/stamp visual alignment, and physical printer output were not end-to-end tested in this environment.
