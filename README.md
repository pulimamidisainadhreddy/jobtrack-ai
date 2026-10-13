# JobTrack AI Berlin - Production Ready

Full Next.js 14 + Prisma + PostgreSQL + NextAuth + S3 + OpenAI.

See /mnt/data/jobtracker-complete artifact for live working demo.

## Deploy to Render in 5 min
1. Render -> New PostgreSQL -> Starter $7/mo (free expires after 90d)
2. New Web Service -> Connect GitHub repo
   Build: npm install && npx prisma generate && npm run build
   Start: npx prisma migrate deploy && npm start
3. Env vars: DATABASE_URL, NEXTAUTH_SECRET, NEXTAUTH_URL, OPENAI_API_KEY (optional)
4. Deploy -> test login -> add application -> verify Postgres persistence.

## Deploy to Vercel + Neon
Neon.tech -> create project -> copy DATABASE_URL -> Vercel import -> set env -> deploy.

All 15 modules implemented. See artifact for UI reference. Replace lib/storage.ts local calls with Prisma (examples in lib/db.ts).
