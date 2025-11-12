# Week 2 Task Brief — React Lagoon

## Core Assignment (4-day build)
Ship the “Krusty Menu Board” React app:
- Fetch menu categories and meals from TheMealDB API on load.
- Provide filters by category and ingredient, plus a search input with debounced queries.
- Allow marking meals as “Crew Favorites” with state lifted to an app context or parent store.
- Track totals (e.g., patties available, favorites count) and surface them in a dashboard header.

## Supporting Focus (1-day drill)
- Create a reusable `ResidentCard` component (SpongeBob, Patrick, Squidward) to practice props, TypeScript interfaces/types, and composition. Keep this under `week-2/components-lab/` and reuse the same component in the core app if helpful.

## Stretch Ideas
- Add client-side routing (React Router) to split views between Menu, Favorites, and Crew.
- Write a React Testing Library spec covering the filter logic or favorite toggles.

## Deliverables
- Repo structure: `week-2/app/` for the Menu Board, `week-2/components-lab/` for the drill.
- **Git Flow workflow**: All code submitted via feature branches with pull/merge requests to `develop` branch (see [Git Flow guide](../assets/gitflow-workflow.md)).
- Project README highlighting data fetching patterns, state management decisions, and how favorites persist.
- Optional Loom (≤2 min) walking through the filtering and favorites experience.

## Reference Materials
- freeCodeCamp React Handbook (core reading for the week).
- React docs: `https://react.dev/learn` sections on components, props, state, and lists.
- TypeScript Handbook: `https://www.typescriptlang.org/docs/handbook/intro.html` (focus on types, interfaces, and React integration).
- React TypeScript Cheatsheet: `https://react-typescript-cheatsheet.netlify.app/` (essential reference for React + TypeScript patterns).
- TheMealDB API docs: `https://www.themealdb.com/api.php`.
- Internal assets: [`gitflow-workflow.md`](../assets/gitflow-workflow.md), [`menu-board-wireframe.md`](../assets/week2/menu-board-wireframe.md), [`resident-card-contract.md`](../assets/week2/resident-card-contract.md).

---

**Navigation:** [Week 2 Overview](../stages/2.md) · [Program Overview](../README.md)

