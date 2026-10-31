# v1.7.10 — Server Signature Font Library

- Replaces browser-only IndexedDB font library with authenticated server library.
- Global fonts are Developer-managed and available to all Dealers.
- Dealer-private fonts are available to all users within the owning Dealer.
- TTF, OTF, WOFF and WOFF2; 5 MB maximum per font.
- Font files load through authenticated Worker API and are stored in Cloudflare R2.
- Font metadata and access scope are stored in D1.
- Existing exact-font rendering, size control, transparent PNG, signature save and Form 34 behavior retained.
- Requires Auth Worker v8, D1 migration and R2 binding FONTS.
