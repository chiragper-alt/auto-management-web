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
