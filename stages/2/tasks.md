# Stage 2 Task Brief — State, Styling, and Advanced Components

## Core Assignment: "Krusty Menu Board" (5-day build)

Build a comprehensive menu board application that demonstrates all Stage 2 concepts.

### Requirements

#### 1. State Management
- Use `useState` for local component state (search queries, filters, UI toggles)
- Implement Zustand store for global favorites state
- Practice state lifting for shared filter state between components
- All state properly typed with TypeScript

#### 2. Array Operations & Filtering
- Fetch menu categories and meals from TheMealDB API
- Implement search functionality with debounced input
- Create filters by category and ingredient using `filter()` and `map()`
- Display filtered results with proper keys
- Calculate derived state (total meals, favorites count) using array methods

#### 3. Styling & Layout
- Set up SCSS/SASS in your project
- Use Flexbox for component layouts
- Implement responsive design (mobile-first approach)
- Apply Tailwind CSS for utility classes and rapid styling
- Create a styled component library (buttons, cards, inputs)
- Practice element positioning for modals or dropdowns

#### 4. React Router
- Set up React Router v6 with TypeScript
- Create routes: `/` (Home), `/menu` (Menu Board), `/favorites` (Favorites)
- Implement navigation with `Link` and `NavLink` components
- Add route parameters for meal detail pages (optional)
- Create shared layout component with navigation

#### 5. Context API
- Create a ThemeContext for dark/light mode (or user preferences)
- Use Context to avoid prop drilling for theme state
- Compare Context usage with Zustand store

#### 6. Debugging
- Install and configure React Developer Tools
- Use DevTools to inspect component props and state
- Profile component re-renders
- Debug state updates and identify unnecessary re-renders

#### 7. Virtual DOM Understanding
- Write components that demonstrate efficient re-rendering
- Use proper keys in lists
- Understand when components re-render and why
- Optimize component structure to minimize re-renders

### Component Structure

```
src/
├── components/
│   ├── Menu/
│   │   ├── MenuBoard.tsx
│   │   ├── MenuFilters.tsx
│   │   ├── MealCard.tsx
│   │   └── MenuBoard.module.scss
│   ├── Layout/
│   │   ├── AppLayout.tsx
│   │   ├── Navigation.tsx
│   │   └── Layout.module.scss
│   └── Favorites/
│       └── FavoritesList.tsx
├── stores/
│   └── favoritesStore.ts (Zustand)
├── context/
│   └── ThemeContext.tsx
├── hooks/
│   └── useDebounce.ts (custom hook)
├── types/
│   └── meal.types.ts
└── pages/
    ├── HomePage.tsx
    ├── MenuPage.tsx
    └── FavoritesPage.tsx
```

## Daily Breakdown

### Day 6: State Management Foundation
- Practice `useState` with multiple state variables
- Build interactive components (counters, toggles, forms)
- Understand state updates and batching
- Type state with TypeScript

**Deliverable:** "Stateful SpongeBob Counter" component with multiple interactive elements

### Day 7: Arrays & Filtering
- Fetch data from TheMealDB API
- Implement search with debouncing
- Create category and ingredient filters
- Use array methods (filter, map, reduce) for data manipulation
- Install and use React DevTools

**Deliverable:** Searchable and filterable menu list

### Day 8: Styling & Layout
- Set up SCSS in project
- Create responsive layouts with Flexbox
- Style components with SCSS modules
- Add Tailwind CSS and use utility classes
- Practice element positioning

**Deliverable:** Fully styled menu board with responsive layout

### Day 9: Routing & Context
- Set up React Router with TypeScript
- Create multiple pages and navigation
- Implement Context API for theme
- Compare Context with local state

**Deliverable:** Multi-page app with routing and theme context

### Day 10: Zustand & Integration
- Create Zustand store for favorites
- Integrate Zustand with existing components
- Complete the full menu board application
- Final styling and polish

**Deliverable:** Complete "Krusty Menu Board" app with all features

## Supporting Labs

### Lab 1: React DevTools Exploration
- Install React Developer Tools
- Inspect component tree
- Monitor state changes
- Profile component performance
- Document findings in README

### Lab 2: Virtual DOM Exercise
- Create components that demonstrate re-rendering
- Use React DevTools to visualize re-renders
- Optimize components to reduce unnecessary renders
- Write a brief explanation of Virtual DOM in your README

### Lab 3: Styling Comparison
- Build the same component with:
  - Plain CSS
  - SCSS Modules
  - Tailwind CSS
- Compare approaches and document preferences

## Stretch Ideas
- Add route parameters for meal detail pages (`/menu/:mealId`)
- Implement protected routes (require authentication)
- Create custom hooks for API fetching
- Add animations with CSS transitions or Framer Motion
- Implement infinite scroll for meal list
- Add unit tests for filter logic using React Testing Library

## Deliverables
- **Repo structure:** All code in the same repository, organized by feature branches
- **Git Flow workflow:** All code submitted via feature branches with pull/merge requests to `develop` branch (see [Git Flow guide](../../guides/gitflow-workflow.md))
- **Project README** with:
  - Setup instructions (SCSS, Tailwind, React Router)
  - State management decisions (when to use useState vs Zustand vs Context)
  - Styling approach documentation
  - React DevTools usage notes
  - Virtual DOM insights
- **At least 3 merged PRs** demonstrating:
  - State management implementation
  - Routing setup
  - Styling system
- Optional: Screen recording demonstrating React DevTools usage

## Reference Materials
- React docs: `https://react.dev/learn` (State, Rendering, Lists, Preserving and Resetting State)
- React Router docs: `https://reactrouter.com/en/main`
- Zustand docs: `https://docs.pmnd.rs/zustand/getting-started/introduction`
- Tailwind CSS docs: `https://tailwindcss.com/docs`
- SCSS documentation: `https://sass-lang.com/documentation`
- React DevTools: `https://react.dev/learn/react-developer-tools`
- TheMealDB API docs: `https://www.themealdb.com/api.php`
- Internal assets: [`gitflow-workflow.md`](../../guides/gitflow-workflow.md), [`menu-board-wireframe.md`](assets/menu-board-wireframe.md), [`resident-card-contract.md`](assets/resident-card-contract.md)

---

**Navigation:** [Stage 2 Overview](topics.md) · [Stage 1: React Basics](../1/topics.md) · [Stage 3: Advanced Patterns](../3/topics.md) · [Program Overview](../../README.md)
