Auto Management Web v1.5.09 — Form 34 UI Only

Change summary:
- Removed Form 34 generation, customer-data mapping, financer/stamp lookup, IndexedDB persistence, saved-status detection, preview modal, and print functionality from the Web Documents UI script.
- Kept the Form 34 document box, status text, Generate Form 34 button, and Preview icon as visual UI elements only.
- Form 34 status now states that functionality has been removed.
- Other document upload and customer signature functionality is unchanged.

Validation:
- ZIP integrity checked after packaging.
- All 16 inline JavaScript blocks passed Node.js syntax checking.
- Browser runtime testing not performed.
