# Auto Management Web v1.5.03 — Form 34 Field Mapping Fix

- Corrected Form 34 data mapping to use the actual flat Customer Record schema (e.g. `assignedOffice`, `branchAddress`, `financerCity`, `hypothecationDate`).
- Added mapped owner/father/address, vehicle engine/model/class, registration/invoice, and loan account details to the generated Form 34.
- Preserved Financer Master as the source for financier name/address/stamp.
- This is a code-level mapping fix; browser workflow should be verified with the user's local record.
