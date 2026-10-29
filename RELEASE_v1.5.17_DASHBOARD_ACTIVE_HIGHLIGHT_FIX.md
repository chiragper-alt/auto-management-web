# v1.5.17 — Dashboard Active Highlight Fix

- Sidebar active state is synchronized before page rendering, including the static Dashboard branch that returns early.
- Uses the exact `data-page` value rather than matching visible text.
- Restores a consistent blue active background and visible keyboard focus.
- Based on v1.5.16; no feature modules intentionally removed.
