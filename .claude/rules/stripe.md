---
globs:
  - "src/**/stripe*"
  - "supabase/functions/*stripe*"
  - "supabase/functions/*webhook*"
  - "stripe-fixtures.json"
---
# Stripe

- Unless otherwise specified, set up app with single subscription: $5/mo and coupon "familydiscount": 100% off, forever, unlimited redemptions.
- Feature gating reads from the database, never calls Stripe API at runtime.
