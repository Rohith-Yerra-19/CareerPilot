# CareerPilot MVP

CareerPilot is a local-first career coaching dashboard. It combines a polished React/Vite UI with a FastAPI API for profiles, resume uploads, deterministic skill-gap analysis, roadmaps, interview practice, and progress tracking.

## Quick start

### Backend

```powershell
cd backend
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

### Frontend

```powershell
cd frontend
npm install
npm run dev
```

Open http://localhost:5173. The Vite dev server proxies `/api` to FastAPI. Copy `.env.example` to `.env` to configure optional integrations; the MVP works without them.

## API

`GET /api/health`, `POST /api/profiles`, `POST /api/resumes`, `POST /api/analyze`, `GET /api/analysis/{id}`, `POST /api/interview/questions`, and `POST /api/progress`.

Analysis is deterministic and local when no LLM or MongoDB settings are present. JWT helpers are included as an optional auth foundation.
