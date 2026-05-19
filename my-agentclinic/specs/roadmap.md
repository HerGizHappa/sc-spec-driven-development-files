# Roadmap

A walking-skeleton roadmap: each phase ends with the app still running end-to-end. Phases are deliberately small — one concern per phase. Order matters; later phases assume earlier ones.

## Phase 1 — Hello, Next.js

Replace the bare `tsc` scaffold with a Next.js app that renders a single page saying the clinic is open.
- **Done when:** `npm run dev` serves a page in the browser.

## Phase 2 — One real route

Add a `/therapies` page that lists therapies from a hardcoded array in the code.
- **Done when:** visiting `/therapies` shows the list. No database yet.

## Phase 3 — Add SQLite

Wire SQLite into the app (per `tech-stack.md`) and move the therapies list from the hardcoded array into the database. One table, one query.
- **Done when:** `/therapies` reads from SQLite; the hardcoded array is gone.

## Phase 4 — Agents

Add an `agents` resource (the patients). A page that lists agents, backed by the database.
- **Done when:** `/agents` lists agents from the database.

## Phase 5 — Ailments on agents

Each agent has one or more ailments. Show ailments on the agent page.
- **Done when:** opening an agent shows their ailments.

## Phase 6 — Booking: the data

Introduce an `appointments` table linking an agent to a therapy at a time. No UI yet — just the schema and a way to seed test rows.
- **Done when:** appointments exist in the database and can be queried.

## Phase 7 — Booking: the flow

A booking page: pick an agent, pick a therapy, pick a time, submit. Creates a real appointment row.
- **Done when:** a user can complete a booking end-to-end and see it persisted.

## Phase 8 — Staff dashboard, read-only

A `/dashboard` page that shows today's appointments. No auth yet — the page is just unlisted.
- **Done when:** staff can open the dashboard and see what's booked.

## Phase 9 — Auth on the dashboard

Decide on the auth approach (deferred from `tech-stack.md`) and gate `/dashboard` behind a login.
- **Done when:** unauthenticated users cannot reach the dashboard.

## Phase 10 — Marketing surface

A proper home page, written for Steve. Visual polish, the framing from `mission.md`, links into the booking flow.
- **Done when:** the landing page is something Steve will sign off on.

## Phase 11 — Dashboard, interactive

Staff can cancel or reschedule appointments from the dashboard.
- **Done when:** a staff member can manage bookings without touching the database.

## Out of scope (for now)

Payments, multi-clinic support, agent self-service accounts, notifications, analytics. Each of these earns its own phase later — not before Phase 11 lands.
