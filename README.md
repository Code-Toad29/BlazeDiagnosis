# Vehicle Service Platform Skeleton

This archive contains a delivery-oriented starter skeleton for the vehicle service SaaS platform.

## What is now implemented
- Auth starter flow with login and forgot-password service/controller logic
- Customer CRUD starter service/controller/repository pattern
- Vehicle CRUD starter service/controller/repository pattern
- Job creation and status-history starter workflow
- Quote creation, totals calculation, public token generation, and approve/reject starter workflow
- In-memory demo store to let developers trace the full vertical slice quickly
- Frontend feature panels for dashboard, customers, vehicles, jobs, and quotes
- API wrappers aligned to the starter backend contracts

## Still intentionally placeholder
- Real HTTP server and routing framework
- Persistent database integration through Prisma repository implementations
- Queue workers, notifications, invoices, payments, inspections, and collection flows
- Authentication hardening, password hashing, and session persistence
- Full design system and production-grade frontend state management

## Architecture summary
- Frontend: Next.js / React / TypeScript
- Backend: Node.js / TypeScript / Express-style modular monolith pattern
- Database: PostgreSQL
- ORM: Prisma
- Queue/events: Redis/BullMQ-compatible placeholder structure

## Suggested implementation order
1. Replace the in-memory repositories with Prisma-backed repositories.
2. Introduce a real router layer and map controller methods to HTTP endpoints.
3. Add request validation middleware and tenant-aware auth middleware.
4. Implement invoices, payments, notifications, inspections, and collection.
5. Add supplier and marketplace domains only after Phase 1 is stable.

## Demo credentials
- Email: admin@demo-workshop.local
- Password: demo1234


## Auth layer completed in starter

The starter now includes:
- password hashing via Node crypto scrypt
- signed access, refresh, and reset tokens
- refresh session storage in the in-memory demo store
- forgot password and reset password flow
- authenticated `/api/auth/me` endpoint pattern
- frontend auth API wrapper, local session storage, and interactive auth panel

### Demo credentials
- Email: `admin@demo-workshop.local`
- Password: `demo1234`

---

## Repository bootstrap

### Workspace layout
- `backend/` API and domain modules
- `frontend/` Next.js application
- `docs/` product, API, schema, and planning documents
- `.github/workflows/` CI placeholder

### Quick start
1. Copy `.env.example` to `.env`.
2. Copy `backend/.env.example` to `backend/.env` if you want backend-local overrides.
3. Copy `frontend/.env.example` to `frontend/.env.local`.
4. Start local services with `docker-compose up -d`.
5. Install dependencies in each workspace.
6. Run `npm run db:generate`.
7. Run `npm run db:migrate`.
8. Run `npm run db:seed`.
9. Start the backend with `npm run dev:backend`.
10. Start the frontend with `npm run dev:frontend`.

### Current repo foundation status
- Root workspace scripts added.
- Shared env templates added.
- Docker local services added for Postgres and Redis.
- Prisma generate/migrate/seed tooling added.
- GitHub Actions CI placeholder added.

### Still expected later
- Real lint and test runners.
- Root lockfile and dependency installation.
- Production deploy workflows.
- Secrets management per environment.
- Prisma migration history generated from live schema updates.

---

# Student Internship Additions

This repository has been prepared for CTU Bloemfontein interns participating in the Blaze Web Works remote internship.

## Where Interns Should Start

Students should begin with:

1. `STUDENT_START_HERE.md`
2. `docs/internship/REMOTE_INTERNSHIP_PLAN.md`
3. `docs/internship/FIRST_WEEK_TRAINING_SCHEDULE.md`
4. `docs/training/GITHUB_WORKFLOW.md`
5. `docs/training/SOFTWARE_STUDENT_PATH.md` or `docs/training/CYBER_SECURITY_STUDENT_PATH.md`
6. `docs/backlog/STUDENT_STARTER_TASKS.md`

## Internship Groups

Current groups supported by this repository:

- Software Developers / Software Engineers
- Cyber Security Analysts

CAD students should use the separate Synergy Inc. CAD repository. Design students are not part of the current internship intake.

## GitHub Workflow

Students should not commit directly to `main`. Work should be completed on branches and submitted using pull requests.

Recommended branch format:

```text
student/<student-name>/<task-name>
training/<student-name>/<topic>
docs/<short-doc-name>
fix/<short-bug-name>
```

## Technical Alignment Note

The existing repository currently uses Prisma for ORM/database workflow. Earlier planning referenced Drizzle ORM. The project owner or mentor should confirm whether the project will continue with Prisma or migrate to Drizzle before assigning database implementation tasks.

See `docs/technical/ORM_DECISION_NOTE.md`.
