# v1.5.56 — Hero Connect Saved Column Mapping

- Replaced read-only Mapping Settings notes with an editable field-to-source-column mapping table.
- Source-column choices are populated from the selected HSRP Order Excel and SalesBillData worksheets.
- Added Save Mapping and Reset Defaults controls.
- Saved mappings persist in browser-local storage and are reused by subsequent imports.
- Import reconciliation reads the saved field mappings for chassis/VIN, registration number/date, bill number, agent, model, and mobile.
- Registration Number and Registration Date remain mapped to HSRP Order Excel; HSRP Order Dealer Name is deliberately excluded from record data and mapping.
- Mapping Settings remains collapsed after import unless the user opens it.
- Changes are scoped to the Hero Connect module.

Validation: ZIP integrity and Hero Connect JavaScript syntax checked. Full interactive browser regression testing has not been performed.
