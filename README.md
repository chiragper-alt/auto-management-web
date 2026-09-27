# Auto Management Web VAHAN Extension v1.2.1

## API bridge fix
- Uses a direct authenticated page-context bridge via `chrome.scripting` instead of relying on the content-script message bridge for API verification and chassis lookup.
- Reads the same local stores used by Auto Management Web: `am_extension_api_key_v1` and `am_master_records_v1`.
- Finds the Auto Management Web tab by title/URL and supports local `file://` builds when Chrome’s **Allow access to file URLs** is enabled for the extension.
- Chassis lookup is exact after trimming spaces and case normalization.
- Existing persistent chassis, Alt+S, strict Entry-New Registration, and VAHAN automation behavior is preserved.

### First-time local HTML setup
If Auto Management Web is opened as a local `.html` file, open `chrome://extensions`, open this extension’s Details, enable **Allow access to file URLs**, then Reload the extension and refresh Auto Management Web.
