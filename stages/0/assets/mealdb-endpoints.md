# Stage 0 — TheMealDB Endpoint Cheat Sheet

Use these endpoints while building the “Krusty Pantry Explorer.” They all work with the public test key `1`; swap in your own key if you upgrade your plan. Full docs live at [TheMealDB API](https://www.themealdb.com/api.php).

## Core Requests
- **Search meals by name**  
  `https://www.themealdb.com/api/json/v1/1/search.php?s=krabby`  
  Use for the main search input. Handles partial matches; returns `null` when nothing is found.

- **Lookup a meal by ID**  
  `https://www.themealdb.com/api/json/v1/1/lookup.php?i=52772`  
  Helpful for detail views when users click a card.

- **Filter by ingredient**  
  `https://www.themealdb.com/api/json/v1/1/filter.php?i=lettuce`  
  Returns lightweight meal objects (id, name, thumb) for quick list rendering.

- **List all ingredients**  
  `https://www.themealdb.com/api/json/v1/1/list.php?i=list`  
  Use to prime dropdowns or validate search terms.

## Response Shape Notes
- Each successful request nests data under a top-level key (`meals`).
- Missing data returns `{"meals": null}` — treat it as an empty array in the UI.
- Images can be resized by adding `/preview` before the filename extension.

## Integration Tips
- Debounce search requests (250–400ms) to avoid spamming the API.
- Cache the latest response in memory to keep the interface snappy.
- Compose ingredient thumbnails using:  
  `https://www.themealdb.com/images/ingredients/<Ingredient>-Small.png`

---

**Related Task:** [Stage 0 Task Brief](../../tasks.md)

