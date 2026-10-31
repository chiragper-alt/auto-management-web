# Auto Management Web v1.6.99 — Final Payment Flow

Based on v1.6.98 Dealer Edit Save Fix.

## Included
- Developer can issue a payment bill to an active Dealer by selecting Dealer and subscription plan.
- Bill amount is calculated server-side from the selected active plan; client-submitted amounts are not trusted.
- Dealer sees the issued bill, due date, message, UPI mobile number 9512907008 and payment instructions.
- Dealer submits payment method, UTR/reference and paid date against the issued bill.
- Developer approves or rejects the payment manually.
- Approval activates/renews the subscription and marks the bill paid.
- Rejection reopens the bill for resubmission.
- Existing payment history and subscription summary remain available.

## Deployment
1. Apply `subscription_final_payment_flow_migration.sql` to the existing D1 database once.
2. Deploy Auth Worker v6, preserving the existing `DB` binding and Worker URL.
3. Deploy this frontend package through the existing GitHub/Cloudflare Pages/Workers Static Assets workflow.
4. Test with a non-production Dealer account: issue bill → Dealer submits UTR → Developer approves → verify subscription expiry and bill status.

Customer records and local documents are not modified by this feature.
