# v1.5.53 — Master Record Active State Fix

- Fixed sidebar active-item matching for the Master Records page.
- Navigation now matches the page using `data-page`, rather than label text substring matching, so the singular sidebar label "Master Record" correctly activates for the plural page name "Master Records".
- The shared `.nav-item.active` blue styling now applies consistently.
