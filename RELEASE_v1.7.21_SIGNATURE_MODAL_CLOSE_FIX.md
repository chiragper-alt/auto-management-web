# v1.7.21 — Signature Modal Close Fix

- Binds an independent close handler immediately after the signature modal is inserted.
- Close button uses a direct onclick handler and stops event propagation.
- Adds backdrop click and Escape-key close handling in capture phase.
- Preserves the existing close listener as fallback and retains v1.7.20 labels and Global Font default.
