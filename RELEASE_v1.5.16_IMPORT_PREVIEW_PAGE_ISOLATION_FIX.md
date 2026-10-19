# Auto Management Web v1.5.16 — Import Preview Page Isolation Fix

- Clean up Import Center PDF mapping preview and saved-format modal before navigating to any other page.
- Clear active PDF preview canvas, mapping state, and temporary PDF object URLs on page teardown.
- Guard asynchronous PDF.js rendering so a render started on Import Center cannot continue updating UI after navigation.
- Preserve existing Import Center mapping/templates and other application modules.

Validation: ZIP integrity and inline JavaScript syntax checks. Full live-browser interaction testing has not been performed.
