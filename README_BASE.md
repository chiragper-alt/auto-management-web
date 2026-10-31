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


## v1.4.46 — Financer Master Dropdown Fix
- Customer Details Hypothecation Financer Name is a visible native select populated from the same `am_financers_v1` list as Sidebar → Financer.
- Added shared API and local storage fallbacks, selected ID/name matching, and auto-fill of branch address, city/district, state and pincode.
- Added an inline count/help message so an empty list is diagnosable.

## v1.4.57 — Hypothecation Toggle Persistence Fix
- Hypothecation ON/OFF now persists immediately to the same Customer/Vehicle Master Record when the switch changes.
- Save Details continues to save the Hypothecation state and all HPA address/date fields together.
- No separate Financer ID is retained on the customer record.

## v1.4.58 — Hypothecation Financer Name/Address Persistence Fix
- Save Customer Details persists the selected Financer Master display name (never the dropdown's internal option ID) and all current Hypothecation address/date fields to the same Customer/Vehicle record.
- Added robust selected-financer resolution by ID first, then normalized name, and expanded address aliases for fallback values.
- Financer remains attached to the existing Customer Record; no separate Financer ID is required on the customer record.

## v1.4.59 — Customer Details Save Feedback
- Added prominent green “Saved Successfully” status for verified Customer Details saves.
- Save button now visibly changes to “✓ Saved Successfully” after successful verification.
- Save failures show a prominent error status instead of silent UI feedback.
- Preserves Customer ID based records, Hypothecation persistence, and live Financer address autofill.


### v1.4.60 — Save button dirty-state tracking
- After a verified save, the success state remains visible until the user edits a Customer Details or Hypothecation field.
- Any subsequent field edit or financer selection clears the old success message and restores the normal “Save Details” button.
- Shows an “Unsaved changes” message until the next verified save.
