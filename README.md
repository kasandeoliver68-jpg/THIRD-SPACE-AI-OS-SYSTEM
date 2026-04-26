# ThirdSpace AI OS

ThirdSpace AI OS is an autonomous institutional command center for turning a single submission into a full intelligence workflow.

The system is designed around one rule:

> Submit once. ThirdSpace AI OS orchestrates the rest.

It accepts tenders, donor calls, policy documents, public budgets, market opportunities, startup ideas, investor mandates, business proposals, sector reports, pasted text, file placeholders, and URL placeholders. From that single input, the OS can automatically classify the signal, generate strategic intelligence, build venture concepts, produce positioning documents, match investors, store everything in the knowledge base, and queue human approval requests where the action is high risk.

## What It Does

The autonomous workflow is:

1. Input submission
2. Auto classification
3. Signal capture
4. Intelligence analysis
5. Venture generation
6. Validation
7. Positioning document generation
8. Investor matching
9. Knowledge base storage
10. User notification

The prototype implements the seven OS layers:

- Signal Capture
- Intelligence Engine
- Knowledge Base
- Automation Grid
- Positioning Engine
- Venture Studio
- Capital Engine

It also includes the three core AI operators:

- Policy Analyst
- Venture Architect
- Deal Structurer

## Repository Structure

- [frontend/src/App.jsx](frontend/src/App.jsx)
- [frontend/src/main.jsx](frontend/src/main.jsx)
- [frontend/src/pages](frontend/src/pages)
- [backend/src/app.js](backend/src/app.js)
- [backend/src/server.js](backend/src/server.js)
- [backend/src/services](backend/src/services)
- [backend/prisma/schema.prisma](backend/prisma/schema.prisma)
- [backend/prisma/seed.js](backend/prisma/seed.js)

## Tech Stack

Frontend:
- React
- Vite
- Framer Motion
- Lucide React
- Recharts
- Tailwind CSS dependencies are included for future expansion, while the current prototype uses a custom glassmorphism stylesheet for the command-center look.

Backend:
- Node.js
- Express.js
- Prisma ORM schema for SQLite prototype mode
- JWT auth placeholder
- Mock AI fallback when no OpenAI key is present

## Setup

Install dependencies from the repository root:

```bash
npm install
```

## Run

Start both apps together:

```bash
npm run dev
```

Frontend only:

```bash
npm run dev --workspace frontend
```

Backend only:

```bash
npm run dev --workspace backend
```

The frontend runs on `http://localhost:5173` and proxies `/api` requests to the backend on `http://localhost:4000`.

## Build

Build both workspaces:

```bash
npm run build
```

## Backend Commands

From the repository root:

```bash
npm run build --workspace backend
npm run start --workspace backend
npm run db:push --workspace backend
npm run db:seed --workspace backend
```

Backend environment variables live in [backend/.env.example](backend/.env.example).

## Frontend Commands

```bash
npm run dev --workspace frontend
npm run build --workspace frontend
npm run preview --workspace frontend
```

## Prisma And SQLite

The prototype includes a complete Prisma schema for SQLite in [backend/prisma/schema.prisma](backend/prisma/schema.prisma).

The seed script in [backend/prisma/seed.js](backend/prisma/seed.js) is included for prototype data bootstrapping. The runtime prototype also ships with an in-memory store so the autonomous workflow works immediately without requiring a database migration first.

Recommended local database flow:

```bash
npm run db:push --workspace backend
npm run db:seed --workspace backend
```

## Mock AI Mode

The backend works even if `OPENAI_API_KEY` is missing.

When no OpenAI key is configured, the system uses realistic mock outputs for:

- signal classification
- strategic summary
- opportunity gap analysis
- policy relevance
- risk analysis
- opportunity score
- venture concept generation
- validation planning
- executive summary
- policy brief
- investment memo
- pitch deck outline
- investor matching notes
- approval request generation

The sample Uganda mini-grid PPP input is pre-seeded so the UI shows a realistic autonomous pipeline immediately.

## OpenAI Connection

To connect a real OpenAI key:

1. Set `OPENAI_API_KEY` in `backend/.env`
2. Optionally set `OPENAI_MODEL`
3. Restart the backend

Example:

```bash
OPENAI_API_KEY=sk-...
OPENAI_MODEL=gpt-4.1-mini
```

If the key is missing or the request fails, the backend falls back to mock AI responses automatically.

## Human Approval Rules

ThirdSpace AI OS is allowed to automatically:

- classify
- analyze
- summarize
- score
- generate briefs
- generate ventures
- generate reports
- match investors
- store knowledge
- notify the user

ThirdSpace AI OS must not automatically:

- send investor emails
- sign contracts
- approve funding
- move money
- publish official reports
- delete critical records
- make legal commitments

Those actions are routed to the Human Approval Center.

## Auth

The backend includes JWT auth endpoints under `/api/auth`.

This prototype uses a demo-friendly auth flow so the command center can be exercised without a full identity provider.

## Notes

- The frontend landing page explains the seven OS layers and the autonomous workflow.
- The Autonomous Intake page submits one form and then redirects to the Live OS Processing view.
- The Live OS Processing page shows simulated stage progression, operator activity, real-time logs, and a final result preview.
- The Dashboard, Knowledge Base, Capital Engine, Reports, and Settings pages are populated with realistic prototype data.

## Sample Input

The seed data is built around this sample opportunity:

> Uganda Ministry of Energy has announced a renewable energy mini-grid PPP opportunity targeting rural electrification with donor support.

That sample is used to demonstrate the full autonomous path from signal capture to approval gating.
# THIRD-SPACE-AI-OS-SYSTEM
# THIRD-SPACE-AI-OS-SYSTEM
