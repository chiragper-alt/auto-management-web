# v1.7.24 — Restore UI After Global Style Regression

- Removed the v1.7.23 global control stylesheet that was inserted without a closing style tag.
- Restored the correct HTML head/body boundary; the malformed style block had caused the rest of the document markup to be parsed as stylesheet content.
- Reverts global button/search/input/select shape overrides to the prior v1.7.22 UI.
- Preserves all v1.7.22 features, including Profile menu removal, signature modal close handling, documents UI, Form 34, and signature font options.
- No JavaScript, authentication, API, D1, or customer data logic changed.
