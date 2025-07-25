# CoolWebsites 🌐

CoolWebsites is a full-stack web application that lets users discover and search for lesser-known but useful, interesting, or fun websites.

---

## 🧱 Tech Stack

| Layer     | Technology         |
|-----------|--------------------|
| Frontend  | React + TypeScript + Tailwind CSS (Vite) |
| Backend   | FastAPI (Python 3.11) |
| Database  | PostgreSQL (Supabase hosted) |
| Hosting   | - Frontend: Vercel (planned)  
             - Backend: Railway (in progress)  
             - Database: Supabase (active) |

---

## ✅ Current Project Status

- ✅ **Frontend** built using React + Vite
- ✅ **Backend** built using FastAPI with pgvector support
- ✅ **PostgreSQL database** hosted on [Supabase](https://supabase.com/)
  - Vector search enabled with `pgvector`
  - Data successfully migrated using `pg_dump` and Supabase SQL Editor
- ✅ `.env` variables prepared for backend and frontend
- ⚙️ **Backend Deployment** in progress via [Railway](https://railway.app/)
  - Facing Nixpacks conflict due to `docker-compose.yml` — fixing by isolating backend directory
- 🕸️ **Frontend Deployment** to be done using [Vercel](https://vercel.com/)

---

## 📁 Project Structure

```bash
.
├── backend/                # FastAPI backend app
│   ├── main.py             # API entry point
│   ├── requirements.txt
│   └── Dockerfile
├── frontend/               # React + Tailwind + TypeScript app
│   ├── src/
│   ├── index.html
│   └── vite.config.ts
├── docker-compose.yml      # [Currently unused] Local dev compose file
└── .gitignore
