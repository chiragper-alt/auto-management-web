# v1.5.55 — Hero Connect Import Workflow Fix

- Removed the duplicate row-by-row preview from Data Import; imported records are displayed in HSRP Record only.
- Replaced “Read files & preview match” and separate confirm action with one “Import” button.
- Added a collapsed Mapping Settings disclosure after a successful import.
- “Clear selection” clears only the selected HSRP/SalesBillData files and import summary/settings; existing imported HSRP records remain unchanged.
- Preserved Hero Connect module isolation and existing source rules, including Registration Number/Date from HSRP Order Excel and ignoring Order Dealer Name.
