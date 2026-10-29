# v1.6.57 — Purchase/Delivery Date Only Mapping

- Removed the separate `Bill Date` field from Excel Customer Import mapping.
- Kept `Purchase / Delivery Date` as the single date mapping field.
- Date normalization now applies only to `purchaseDeliveryDate`.
- Existing import fields and saved mapping key remain unchanged.
