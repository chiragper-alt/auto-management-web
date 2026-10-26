# Auto Management Web v1.5.76 — Purchase Invoice Documents Display Fix

- Fixed the Documents page so it loads previously saved files from `AM_VAHAN_DOCUMENTS_V1` for the currently selected customer record.
- Saved invoice PDFs with `documentKey: invoice` are displayed in the **Purchase Invoice** box with the saved filename and a Saved indicator.
- Saved customer signature records using `customerSignature` are mapped to the Customer Signature box when loading existing documents.
- The display is driven by the local IndexedDB document database and remains local to the browser/device.
- Validation: all 15 inline scripts pass Node syntax checks and the ZIP archive passes `unzip -t`.
- Browser end-to-end testing against real customer data remains required.
