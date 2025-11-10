# Week 2 Task Brief — React Lagoon

## Core Assignment (4-day build)
Ship the “Krusty Menu Board” React app:
- Fetch menu categories and meals from TheMealDB API on load.
- Provide filters by category and ingredient, plus a search input with debounced queries.
- Allow marking meals as “Crew Favorites” with state lifted to an app context or parent store.
- Track totals (e.g., patties available, favorites count) and surface them in a dashboard header.

## Supporting Focus (1-day drill)
- Create a reusable `ResidentCard` component (SpongeBob, Patrick, Squidward) to practice props, typing (PropTypes or TypeScript), and composition. Keep this under `week-2/components-lab/` and reuse the same component in the core app if helpful.

## Stretch Ideas
- Add client-side routing (React Router) to split views between Menu, Favorites, and Crew.
- Write a React Testing Library spec covering the filter logic or favorite toggles.

## Deliverables
- Repo structure: `week-2/app/` for the Menu Board, `week-2/components-lab/` for the drill.
- Project README highlighting data fetching patterns, state management decisions, and how favorites persist.
- Optional Loom (≤2 min) walking through the filtering and favorites experience.

## Reference Materials
- freeCodeCamp React Handbook (core reading for the week).
- React docs: `https://react.dev/learn` sections on components, props, state, and lists.
- TheMealDB API docs: `https://www.themealdb.com/api.php`.
- Internal assets: [`menu-board-wireframe.md`](../assets/week2/menu-board-wireframe.md), [`resident-card-contract.md`](../assets/week2/resident-card-contract.md).

---

**Navigation:** [Week 2 Overview](../stages/2.md) · [Program Overview](../README.md)

