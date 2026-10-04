Auto Management Web V1.4.0 — Settings & Status Polish

Changes in this build:
- Removed Export, VAHAN Automation and Notifications options from Settings navigation.
- Removed the generic "Dashboard" fallback button from internal pages; navigation is handled by the sidebar.
- Added distinct visual colors for Ready, OTP Ready, In Progress, Completed, Document Pending and Partial statuses across record views.
- Application Settings are now functional and saved locally: Dealer Name, Dealer Code, Startup Dashboard and Auto-save Changes.
- Dealer Name and Dealer Code changes update the sidebar identity.
- Startup Dashboard can be enabled/disabled; when disabled, the last opened page is restored on startup.
- Preserved the v1.3.9 standalone monogram SVG single-render fix.

# Auto Management Web v1.4.17 — Bulk Invoice PDF Import

## Added
- Compact Invoice PDF Import section in Import Center.
- Bulk selection and drag-and-drop for multiple PDF invoices.
- Browser-side text extraction using PDF.js loaded on demand.
- OCR fallback for scanned PDFs using Tesseract.js loaded on demand (up to the first five pages per PDF).
- Heuristic extraction for customer, mobile, chassis, engine, invoice number, sale amount, model, address, GSTIN and dealer name.
- Editable review queue, per-file status, duplicate-chassis checks, and explicit user confirmation before saving.
- Approved records are saved through the existing `AMData` record store; current Excel/CSV import remains available.

## Requirements and limitations
- PDF.js and OCR libraries are loaded from public CDNs when first needed, so an internet connection is required for the first load and OCR fallback.
- Extraction is heuristic and dealer layouts vary. Users must verify the values against each original invoice before import.
- OCR currently attempts English recognition and up to five pages per scanned PDF. Multi-language or unusually formatted invoices may need manual review.
- Invoice PDFs are processed in the browser; this feature does not upload them to a separate application server.
- PDF binaries are not attached to the resulting master record; only extracted record fields are saved.


# Auto Management Web v1.4.23 — Local Document Inbox

## Added
- New Document Inbox page for computer-first WhatsApp document intake.
- Manual bulk import of PDF/JPG/JPEG/PNG/WEBP files.
- Caption, separate WhatsApp message, and document-type fields per import batch.
- Local IndexedDB storage for imported original files and queue metadata.
- Customer suggestions based on existing local Master Records; operator confirmation required before assignment.
- Folder selection and repeated scanning while the Document Inbox page remains open in a supported browser.
- Duplicate scan suppression for the selected folder using filename, size, and modified time metadata.

## Limitations
- This does not read WhatsApp group messages or captions automatically. Copy/paste the caption and separate message when importing.
- Folder scanning runs only while the app and Document Inbox remain open; this is not a background OS service. Browser folder access requires explicit user permission and a supported desktop browser.
- Files are stored in browser IndexedDB on this computer, not as files in a user-selected permanent filesystem folder. Browser profile clearing can remove local data; export/backup before clearing browser data.
- Confirmed items are linked to the customer record as metadata; existing Saved Documents viewer integration for these new Inbox binaries is not yet complete.
- No end-to-end tests against live dealer records or all browser environments have been performed.


### v1.4.24 Smart filename matching
- Document Inbox customer suggestions now compare partial name tokens from the file name, even when the name is abbreviated or surname/name order differs.
- Ignores common document words (such as invoice, insurance, proof, PDF/JPG) to reduce accidental matches.
- Mobile/chassis exact matches remain stronger than partial-name matches. Please confirm the selected customer before saving, especially for short names or duplicate surnames.


## v1.4.25 — Form 22 OCR and chassis matching
- Document Inbox document type includes Form 22 — Roadworthiness Certificate.
- Bulk import scanned PDF/image files, run OCR, extract a likely 17-character chassis/VIN value, and match against Master Records chassis number.
- Search the inbox by chassis number; verify suggested customer before saving.
- OCR uses PDF.js and Tesseract.js loaded by the browser; first use may require internet access. OCR results depend on scan quality and the printed Form 22 layout.
- OCR processes up to the first four PDF pages per file to control processing time. Files remain in local browser IndexedDB as in the existing inbox implementation.
- ZIP and JavaScript syntax checks do not replace end-to-end testing against the user's real records and scanned Form 22 samples.


## v1.4.26 — Inventory Records + Form 22 linking
- Added separate Inventory Records menu. Import stock once from CSV/XLSX; customer name is optional and chassis number is the linking key.
- Inventory table shows chassis number, engine number, model and whether Form 22 is saved; search by chassis/engine/model and download saved Form 22.
- Bulk select scanned Form 22 PDFs/images, extract chassis using PDF text/OCR, and link the original file to matching inventory chassis. Unmatched documents are retained in local IndexedDB for review (they are not automatically assigned).
- Data is stored locally in this browser profile. Back up/export inventory; clearing browser site data may remove local Form 22 binaries. OCR libraries load from CDN and require internet on first use.
- Import supports CSV and XLSX in this module. Legacy XLS is not supported by this module.

## v1.4.27 — Local database persistence and backup
- Inventory and Form 22 records remain in the local IndexedDB database (`AM_INVENTORY_FORM22_V1`) on this computer/browser profile; no server upload is used by this module.
- Requests persistent browser storage where supported to reduce automatic eviction risk.
- Added a full Inventory + Form 22 local database backup file (`.amwinventory`) including Form 22 binary files, plus restore/merge by chassis number.
- Important: browser IndexedDB is a local browser database, not SQLite. Clearing site/browser data or moving to another computer can still remove/leave behind data unless a backup is restored. For OS-level SQLite storage, the app must run in an Electron/desktop shell or local backend.

## v1.4.28 Document Inbox OCR + Inventory Chassis Linking
- Redesigned the existing Document Inbox bulk-import workflow into a compact review table for mixed WhatsApp-downloaded PDFs and images.
- Each file can be OCR-scanned to suggest a document type (Aadhaar, PAN, Address Proof, Form 20/21/22, Insurance, Invoice, etc.) and detect a chassis number where readable text is present.
- Each imported document has its own document-type selector and Inventory chassis search field; linking requires an exact chassis match and a confirmation prompt.
- Linked files remain in the local Document Inbox IndexedDB and their metadata is attached to the matching Inventory record. Inventory Records includes a View documents action for linked files.
- OCR libraries are loaded from CDN when used; internet access is required on first load. OCR suggestions must be reviewed and manually corrected when necessary.
- Note: this build stores document binaries in the Document Inbox database; the existing Inventory/Form 22 backup file does not yet bundle Document Inbox binaries. Back up the browser profile/database separately until a unified workspace backup is implemented.
