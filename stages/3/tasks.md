# Week 3 Task Brief — Sail to the Surface

## Core Assignment (5-day capstone)
Deliver the “Krusty Krab Dashboard” production-ready app:
- Multi-page experience (Home, Tasks, Menu) with React Router and shared layout components, all typed with TypeScript.
- Task management module using `useState` + `useEffect` with proper TypeScript types, including derived insights (completed counts, overdue flags) and persistence via API or `localStorage`.
- Menu module consuming TheMealDB API with TypeScript interfaces for API responses, caching, loading skeletons, and graceful error recovery.
- Global state strategy (context or lightweight store) with TypeScript type definitions to coordinate tasks, menu favorites, and announcements.
- Deployment pipeline to Render or Vercel with environment notes and API key handling.

## Systems Drill (1-day focus)
- Create a `deploy-checklist.md` covering preflight tests, environment variables, and smoke-test steps. Reuse it during the final deploy demo.

## Stretch Ideas
- Layer in `useEffect` for API polling or side effects (e.g., toast notifications).
- Add a lightweight auth gate (mock login) to demonstrate guarded routes.

## Deliverables
- Repo structure: `week-3/dashboard/` for the capstone and `week-3/deploy-checklist.md`.
- **Git Flow workflow**: All code submitted via feature branches with pull/merge requests. Final release via `release/*` branch merged to `main` (see [Git Flow guide](../../guides/gitflow-workflow.md)).
- README appendix detailing architecture decisions, routing map, and API integration notes.
- Demo outline (bullet list) summarizing problem framing, feature tour, and deployment reflection.

## Reference Materials
- React docs on hooks, effects, and context.
- TypeScript Handbook: `https://www.typescriptlang.org/docs/handbook/intro.html` (advanced types, utility types).
- React TypeScript Cheatsheet: `https://react-typescript-cheatsheet.netlify.app/` (hooks, context, and advanced patterns).
- Vercel/Render deployment guides for React + TypeScript + Vite setups.
- TheMealDB API docs: `https://www.themealdb.com/api.php`.
- Internal assets: [`gitflow-workflow.md`](../../guides/gitflow-workflow.md), [`deploy-checklist-template.md`](assets/deploy-checklist-template.md), [`dashboard-data-flow.md`](assets/dashboard-data-flow.md).

---

**Navigation:** [Week 3 Overview](topics.md) · [Program Overview](../../README.md)

