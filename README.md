# AYXchange code starter

This folder packages the clickable prototype and the starter snippets from the chat. It is **not a complete Next.js app yet**. Use these files inside a Next.js project created with `npx create-next-app@latest ayxchange --typescript --tailwind --eslint --app`.

## Files

- `ayxchange-prototype.html` — clickable design prototype; open it in a browser.
- `src/lib/supabase.ts` — Supabase client helper. Copy into the Next.js project's `src/lib/` directory.
- `supabase/schema.sql` — starter database tables and row-level security policies. Paste into Supabase Dashboard → SQL Editor and run.

## Setup

1. Create a Next.js app and install the Supabase client:

   ```bash
   npx create-next-app@latest ayxchange --typescript --tailwind --eslint --app
   cd ayxchange
   npm install @supabase/supabase-js
   ```

2. Copy `src/lib/supabase.ts` into the Next.js app's `src/lib/supabase.ts`.
3. In Supabase, run `supabase/schema.sql` using the SQL Editor.
4. Create `.env.local` in the Next.js app root with your own project values:

   ```env
   NEXT_PUBLIC_SUPABASE_URL=YOUR_PROJECT_URL
   NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY
   ```

5. Never upload `.env.local` or private keys to GitHub. The anon key is intended for browser use only when row-level security is configured correctly.

The earlier chat also included illustrative snippets for profile saving, mentor discovery, matching, and messages. They need to be wired into actual Next.js pages and tested before this is a production app. In particular, match creation must determine each profile's role before setting `student_id` and `mentor_id`.
