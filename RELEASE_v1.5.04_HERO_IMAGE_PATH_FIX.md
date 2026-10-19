# Auto Management Web v1.5.04 — Dashboard Hero Image Fix

## Root cause
The Dashboard Hero image element had no initial `src`. `applyDealerShowroom()` only assigned an image when dealer-specific browser storage contained a saved photo. With no saved photo, the `<img>` remained source-less while CSS forced it to display, causing the broken-image indicator.

## Fix
- Use the packaged `web/hero_showroom_default.jpg` when no dealer-specific photo is saved.
- If a saved image is invalid/unreadable, fall back to the packaged default.
- Toggle the hero image state only after successful image load.
- Keep dealer-specific uploaded images in local browser storage as before.

## Test status
Static path check and JavaScript syntax check performed. Full live browser interaction testing has not been performed.
