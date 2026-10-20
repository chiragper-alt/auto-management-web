# v1.5.37 — Form 34 Save / Preview Workflow

- Generate Form 34 now creates the document and saves it to the customer-specific local document store (`AM_VAHAN_DOCUMENTS_V1`, key `<recordId>:form34`) and record document metadata; it does not open the document directly.
- The 👁️ button reads the saved Form 34 and opens the preview only when clicked.
- The Financer stamp is larger than the previous build and positioned farther left and upward to keep the “Signature of the financier” label readable.
- PDF/invoice import and unrelated features were not intentionally changed.
- Validation performed: inline JavaScript syntax check and ZIP integrity check. Full browser/device workflow test remains pending.
