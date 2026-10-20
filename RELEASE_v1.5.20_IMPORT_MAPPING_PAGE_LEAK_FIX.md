# Auto Management Web v1.5.20 — Import Mapping Page Leak Fix

## Fixes
- Kept the PDF `Update this layout` mapping panel inside the Import Center wrapper instead of appending it to the whole page view.
- Initialized Import Center against `#page-content`, the container that is replaced during navigation.
- Updated refresh, cancel, and save paths so the mapping panel cannot escape its Import Center wrapper.
- Added explicit cleanup of the mapping panel and Saved Formats modal when navigating away, including any elements previously moved outside the page content.
- Preserved PDF mapping templates, Saved Formats, Import Center and unrelated application features.

## Validation
- ZIP archive integrity checked.
- Inline JavaScript syntax checks performed.
- Browser interaction testing was not available in this build environment; please verify Import Center mapping and navigation in the deployed browser.
