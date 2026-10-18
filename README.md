# Auto Management Web VAHAN Extension v1.2.1

## API bridge fix
- Uses a direct authenticated page-context bridge via `chrome.scripting` instead of relying on the content-script message bridge for API verification and chassis lookup.
- Reads the same local stores used by Auto Management Web: `am_extension_api_key_v1` and `am_master_records_v1`.
- Finds the Auto Management Web tab by title/URL and supports local `file://` builds when Chrome’s **Allow access to file URLs** is enabled for the extension.
- Chassis lookup is exact after trimming spaces and case normalization.
- Existing persistent chassis, Alt+S, strict Entry-New Registration, and VAHAN automation behavior is preserved.

### First-time local HTML setup
If Auto Management Web is opened as a local `.html` file, open `chrome://extensions`, open this extension’s Details, enable **Allow access to file URLs**, then Reload the extension and refresh Auto Management Web.

## v1.4.35 — Document Inbox Code Removal
- Removed the Document Inbox navigation entry, UI styles, initialization hook, IndexedDB module, folder scanning, OCR/document linking code, and Inventory Records links to the Document Inbox database.
- Kept Hero Connect UI-only tabs and existing inventory import/search/backup features.


## v1.4.46 — Financer Master Dropdown Fix
- Customer Details Hypothecation Financer Name is a visible native select populated from the same `am_financers_v1` list as Sidebar → Financer.
- Added shared API and local storage fallbacks, selected ID/name matching, and auto-fill of branch address, city/district, state and pincode.
- Added an inline count/help message so an empty list is diagnosable.
