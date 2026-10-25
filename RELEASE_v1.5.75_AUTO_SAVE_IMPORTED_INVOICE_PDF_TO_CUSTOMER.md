# Auto Management Web v1.5.75 — Auto-save imported purchase invoice PDF

- When a sale-invoice PDF is imported and its extracted record is created, the original uploaded PDF is saved in the local IndexedDB document store under that customer's `invoice` / Purchase Invoice document slot.
- If the chassis number already exists in Master Records, the import matches that existing customer record and attaches the PDF there rather than skipping the attachment.
- The customer's Master Record receives Purchase Invoice document metadata so the invoice appears in the customer's Documents list.
- Uses local browser storage (`AM_VAHAN_DOCUMENTS_V1`); no PDF is uploaded to cloud storage by this change.
- Validation performed: inline JavaScript syntax checks and ZIP integrity check. Full browser interaction (importing a real PDF, opening it in customer documents, and restoring a backup) still requires runtime testing.
