# Auto Management Web v1.7.01 — Sidebar & Document Thumbnail Polish

Based on v1.7.00 Premium UI Polish.

## Changes
- Removed the redundant Dealer/identity card from the sidebar (`.sidebar-dealer`) to reclaim clean navigation space.
- Removed circular outlines/decorations from uploaded document thumbnails and PDF preview areas.
- Applied flat white/soft-grey thumbnail surfaces, subtle rectangular borders and consistent 6–8px corners.
- Kept file names, selection, drag/drop, preview and document assignment behavior intact.

## Deployment
Replace `am588/am527/am_polish/index.html` with this package's index.html and deploy using the existing GitHub + Cloudflare Workers Static Assets setup.
No Worker or D1 changes required.
