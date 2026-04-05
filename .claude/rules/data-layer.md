---
globs:
  - "supabase/**"
  - "src/**/queries.ts"
  - "src/**/actions.ts"
---
# Data Layer

- RLS is enabled on every table. No exceptions.
- Every table has `created_at` and `updated_at` timestamp columns.
- Use soft deletes (`deleted_at` timestamp) unless the entity's `definition.md` explicitly specifies hard deletes.
- Generate TypeScript types after every schema change: `npm run gen:types`.
- Never use the Supabase service role in application code unless the function's `definition.md` documents the exception with justification.
