# Tech stack

## Constraint

Server-side TypeScript. Mary wants a reliable site on a popular stack; the whole team works in TypeScript end to end.

## Recommendation: Next.js (App Router)

We recommend **Next.js** with the App Router, written in TypeScript.

Why this fits the stakeholder brief:

- **Mary (reliable, popular TS stack, staff dashboard):** Next.js is the most widely adopted full-stack TypeScript framework. Server Components plus Route Handlers cover both the staff dashboard and the booking APIs without standing up a separate backend service.
- **Susan (agents / ailments / therapies / appointments):** straightforward CRUD-shaped domain. Next.js Server Actions and Route Handlers map cleanly onto these resources without ceremony.
- **Steve (attractive, modern-browser site):** server-rendered React, easy to make fast and pretty, good story for marketing pages alongside the app.

One framework covers marketing site, booking flow, and staff dashboard. One deploy target. One language across the stack.

## Stack at a glance

| Concern | Choice |
|---|---|
| Language | TypeScript (strict) |
| Framework | Next.js (App Router) |
| UI | React (via Next.js) |
| Runtime | Node.js LTS |
| Database | SQLite |
| Package manager | npm |
| Build | `tsc` for the current scaffold; Next.js build pipeline once the framework is in |

## Database: SQLite

SQLite is the database. A single file, no server to run, no credentials to configure.

This matches our target audience (see `mission.md`):

- **Course students** clone the repo and have a working database immediately — no Postgres install, no Docker, no environment variables to copy.
- **Conference-booth demos** run reliably on a laptop with no network dependency. The database travels with the app.

It also matches the product shape: clinic-scale data (agents, ailments, therapies, appointments) is well within SQLite's comfort zone. If we ever outgrow it, the SQL surface area we'll use is portable enough that swapping engines later is a real option, not a rewrite.

## Deliberately deferred

These choices are real but we are not locking them in this document — they get decided in the roadmap phase where they first matter:

- **Auth** — deferred until the staff dashboard needs a login.
- **Styling system** (Tailwind vs CSS modules vs other) — deferred until Steve's marketing surface starts taking shape.
- **Hosting / deploy target** — deferred until we have something worth deploying.

## What we will not use

- Client-only SPA architectures (React without a server framework). Loses Steve's "attractive site that works well with a modern browser" benefit of SSR and complicates Mary's reliability story.
- Non-TypeScript backends. Out of scope per the engineering brief.
