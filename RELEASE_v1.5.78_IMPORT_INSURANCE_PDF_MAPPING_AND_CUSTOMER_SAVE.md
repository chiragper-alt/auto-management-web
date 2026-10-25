# v1.5.78 — Import + Insurance PDF Mapping

- Renamed the Master Records import action and Import Center heading to **Import**.
- Activated the Insurance tab with multiple insurance PDF selection and drag/drop.
- Reused the live PDF field picker and saved-layout/template mechanism for insurance fields.
- Insurance PDFs are matched to an existing customer by chassis number; the importer does not create a new customer for an unmatched insurance PDF.
- Mapped insurance company, policy number/date, period, IDV and other available policy details are saved to the matched customer record.
- Original insurance PDF is stored in local IndexedDB under the customer's `insurance` document slot and announces `am-document-changed` for Documents UI refresh.
- Local-first: no policy PDF is uploaded to a cloud service by this feature.

Validation: inline JavaScript syntax checks passed (15 script blocks); ZIP integrity check performed. End-to-end browser testing with real insurance PDFs remains necessary. Scanned image-only PDFs require OCR and are not automatically read by this text extraction path; use the live PDF mapping picker for selectable PDF text.
