# v1.5.57 — Hero Connect Mapping Save Fix

- Fixed mapping option hydration so selected-file columns load before saved values are reapplied.
- Added explicit unsaved-change feedback when any mapping dropdown changes.
- Strengthened Save Mapping: validates required chassis and HSRP registration fields, writes the full mapping, and verifies every saved field matches the selected values.
- Improved success/failure status text so browser storage issues are visible instead of appearing to save silently.
- Kept mapping persistence local to this browser and scoped all changes to Hero Connect.
- Preserved HSRP-only source priority for Registration Number and Registration Date; Order Dealer Name remains excluded.

Validation: ZIP integrity and JavaScript syntax checked. Full browser interaction testing remains outstanding.
