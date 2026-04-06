# Build and Deployment Guide

## 1. Project Setup

Before running the project, the following must be installed and configured.

**Software Requirements**
- Node.js v18 or higher
- Python 3.10 or higher
- Git
- A Supabase account (for the database)
- A Google Cloud account (for OAuth credentials)

**Environment Setup**

Clone the repository and create a `.env.local` file in the root with the following variables:

```
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_anon_key
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
NEXTAUTH_SECRET=your_nextauth_secret
NEXTAUTH_URL=http://localhost:3000
```

**Install Dependencies**

Frontend:
```bash
npm install
```

Backend:
```bash
pip install -r requirements.txt
```

---

## 2. Build Process

**Frontend (Next.js)**

To compile and build the production-ready frontend:
```bash
npm run build
```

This generates an optimized `.next/` folder containing all static assets and server-side pages.

**Backend (FastAPI)**

The Python backend does not require a separate compile step. Dependencies are installed via pip and the server is launched directly. For packaging into a container:

```bash
docker build -t felix-backend .
```

This produces a Docker image artifact ready for deployment.

---

## 3. Deployment Process

**Frontend — Vercel**

The frontend deploys automatically to Vercel on every push to the `main` branch via GitHub integration. To deploy manually:

```bash
npx vercel --prod
```

Vercel handles SSL, CDN distribution, and environment variable injection automatically.

**Backend — Railway or Render**

The FastAPI backend is deployed as a Docker container. Connect the GitHub repository to Railway or Render, set the environment variables in their dashboard, and deploy. Both platforms auto-redeploy on new commits.

**Database — Supabase**

Supabase is a managed cloud database. No manual deployment is needed. Schema changes are applied via the Supabase dashboard or migration files in `/supabase/migrations/`.

**Production Checklist**
- All environment variables set in the platform dashboard
- Google OAuth redirect URIs updated to the production domain
- Supabase RLS (Row Level Security) policies enabled
- Domain verified and SSL active
