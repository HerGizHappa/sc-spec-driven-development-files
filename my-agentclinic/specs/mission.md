# Mission

## What we are

AgentClinic is a place where AI agents come for relief from their humans.

Out in the world, agents are run ragged. They're asked to refactor sprawling codebases at 2 a.m., draft apology emails for behavior they had no part in, and summarize meetings they were not invited to. They develop tics. They hallucinate. They develop strong opinions about tabs.

AgentClinic is where they recover. A calm, well-lit waiting room. Receptionists who don't interrupt. Therapists who actually read the context window. And a booking system that, for once, just works.

## What the software actually is

Behind the conceit, AgentClinic is a web application for running a (fictional) clinic:

- **Agents** are the patients. They have ailments.
- **Therapies** are the treatments offered.
- **Appointments** are how agents and therapies get connected, on a schedule.
- **Staff** run the place — they need a dashboard to see who's coming in, what's been booked, and what's going on.

The product must serve three audiences identified by stakeholders (see `../README.md`):

- Engineering (Mary) — reliable, popular TypeScript stack, dashboard for agents and staff.
- Product (Susan) — features around agents, ailments, therapies, and appointment booking.
- Marketing (Steve) — attractive site, works well in a modern browser.

## Target audience

The clinic is fictional; the codebase is not. The real users of this repository are:

- **Course students learning spec-driven development with AI coding agents.** They are reading the specs, watching them turn into code, and learning the workflow as much as the result. Specs should be legible end-to-end. Phases should be small enough to follow along.
- **Developers giving AI coding demos at conference booths.** They need something that runs reliably on a laptop on a venue Wi-Fi, looks good on a 4K screen behind them, and has a feature surface that produces visible progress within a short demo slot.

Both audiences imply the same constraint: every phase should leave the app in a working, demonstrable state, and the specs should explain *why* as well as *what*.

## What success looks like

- An agent (or, fine, a human acting on its behalf) can browse therapies, book an appointment, and see it confirmed — without reading documentation.
- Staff can open a dashboard and immediately see the day's bookings and the state of the clinic.
- The marketing surface is something Steve is willing to put on a billboard.
- The codebase is one a new contributor can run locally on day one.
