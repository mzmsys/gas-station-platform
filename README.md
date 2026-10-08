# Fuel ERP

Records, reconciliation, and reporting for fuel stations.

Stack (MVP): Next.js + React on Vercel, Supabase (Postgres + Auth).

Work is delivered sprint by sprint, story by story. Design notes live in [docs/](docs/).

## Database

Schema changes are versioned SQL migrations in [supabase/migrations/](supabase/migrations/), applied with the Supabase CLI (`npx supabase`).

```sh
npx supabase db start     # local Postgres (needs Docker)
npx supabase db reset     # re-apply all migrations locally
npx supabase test db      # run the tests in supabase/tests/
npx supabase link --project-ref <ref>
npx supabase db push      # apply pending migrations to the hosted database
```
