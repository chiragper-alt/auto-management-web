# Auto Management Web v1.5.92 — HSRP Model Source Fix

- Vehicle Model is now sourced exclusively from the matched SalesBillData row.
- HSRP Order Excel Model mapping is disabled and ignored.
- Default SalesBillData model mapping is `model`; column detection also recognizes model/vehicle description headers.
- Saved legacy mappings cannot override the source: `modelH` is forced blank and no HSRP model fallback is used.
- Other HSRP and SalesBillData mappings and chassis matching behavior are unchanged.

Validation: ZIP integrity and inline JavaScript syntax checks performed. Live import with the user's actual spreadsheets remains to be verified.
