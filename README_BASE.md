# Auto Management Web — VAHAN Workflow

Updated web prototype with a functional local VAHAN workflow connected to Master Records.

## Included
- Auto Management Web branding
- VAHAN record selection from actual Master Records
- Step 1: Record Selection
- Step 2: Data Preparation and required-field validation
- Step 3: Processing state
- Step 4: Verification and Mark Completed
- Local workflow progress save
- Dashboard/Master Records status updates

## Note
This build implements the web-side workflow and data connection. Live interaction with the external VAHAN portal requires a separate authorized server/browser automation integration; this prototype does not claim to perform live portal actions.


## v1.5.0 — Dealer Admin & Operator Access
- Dealer Admin ID/password login with salted password hashes.
- Operator ID creation/edit/enable/disable and module permissions.
- Current dealer/operator identity shown in the workspace and audit metadata on record changes.
- Connected `.amdb` database files persist dealer/operator workspace metadata alongside records.
- Existing local records and VAHAN workflow remain compatible.
