# v1.7.27 — Signature Initialization and Auth Scope Fix

Root cause: the Documents/Signature code is in a separate IIFE from the authentication module. It referenced the auth module's lexical `session` variable directly. That identifier is out of scope and throws `ReferenceError: session is not defined` when opening the Signature modal, after modal markup is inserted but before preview, draw, clear, save, and font event handlers are initialized.

Fixes:
- Retrieve auth state only through the published `window.__amAuthGetSession()` API.
- Bind Signature entry buttons before optional document controls.
- Guard optional DOM elements so one missing control cannot abort all event binding.
- Keep Worker/D1/R2/auth implementation and other modules unchanged.

Browser end-to-end verification against the live deployment remains required.
