# v1.6.89 — Dealer Delete Option

- Added a Delete action to each Dealer row.
- Requires explicit browser confirmation before deletion.
- Removes the Dealer registry record and its associated Operator login records from this browser's local storage.
- Clears active Dealer workspace selection if the deleted Dealer was active, then selects another active Dealer if available.
- Does not delete vehicle/business records. Dealer registry is currently localStorage-based, not D1-synced.
- Based on v1.6.88.
