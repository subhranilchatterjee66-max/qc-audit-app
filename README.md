# Academic QC Audit Web App

A full-stack prototype for strict postgraduate academic quality control. It accepts an assignment brief, marking rubric, and student submission, extracts text, sends it to an AI QC engine, and returns a structured audit report with HD readiness, score estimation, rubric gaps, and final verdict.

## Stack

- Frontend: React + Vite + Tailwind CSS
- Backend: Node.js + Express
- AI Engine: Python + FastAPI + OpenAI
- Database: PostgreSQL schema included

## Folder Structure

```bash
qc-audit-app/
├── frontend/
├── backend/
├── python-engine/
└── database/
```

## Quick Start

### 1. Python QC Engine

```bash
cd python-engine
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

Add your OpenAI API key in `.env`.

### 2. Backend

```bash
cd backend
npm install
cp .env.example .env
npm run dev
```

Backend runs on `http://localhost:5000`.

### 3. Frontend

```bash
cd frontend
npm install
npm run dev
```

Frontend runs on `http://localhost:5173`.

## Important Note

The QC system uses AI judgement. It is designed to support human academic quality control, not replace final academic marking.
