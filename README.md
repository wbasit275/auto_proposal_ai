# Auto Proposal AI — Ready-to-Deploy (Free-tier first)

This archive contains a deployable **free-tier first** version of *Auto Proposal AI*:
- Frontend: React + Vite (deploy to Vercel)
- Backend: Express (deploy to Render or Vercel Serverless)
- Auth & DB: Supabase (free tier)
- AI: OpenRouter (free tier) — replaceable with other providers

## Quick local run (dev)

### Backend
```bash
cd backend
npm install
cp .env.example .env
# fill .env with your SUPABASE + OPENROUTER keys
npm start
```

### Frontend
```bash
cd frontend
npm install
cp .env.example .env
# fill .env with VITE_SUPABASE_URL, VITE_SUPABASE_KEY, VITE_BACKEND_URL
npm run dev
```

## Deploy
- Frontend: push `frontend/` to GitHub and connect to Vercel.
- Backend: push `backend/` to GitHub and connect to Render (or Vercel serverless).
- Create a Supabase project and run the SQL in `backend/supabase-schema.sql` to create the `usage` table.
- Create an OpenRouter account and put the key in backend `.env`.
- For production, configure environment variables in Vercel/Render settings from `.env.example`.

## Files included
- backend/ — Express API, proposal generation, PDF export
- frontend/ — React app with login (Supabase) + proposal generation UI
- docs/prompt-templates.md — starter prompts
- infra/ — deployment notes
- .gitignore, .env.example templates

If you want, I can now deploy this for you (I’ll provide exact Vercel/Render steps).