# Stage 3 Task Brief — Advanced Hooks, Patterns, and Deployment

## Core Assignment: "Krusty Krab Dashboard" (5-day capstone)

Build a production-ready management dashboard that demonstrates mastery of all React concepts learned throughout the bootcamp.

### Requirements

#### 1. Advanced Hooks & Custom Hooks
- Use `useEffect` for:
  - API data fetching with proper cleanup
  - Subscriptions and event listeners
  - localStorage synchronization
  - Side effects with dependency arrays
- Create custom hooks:
  - `useLocalStorage` for persistent state
  - `useFetch` or `useApi` for data fetching
  - `useDebounce` for search inputs
- All hooks properly typed with TypeScript

#### 2. Advanced State Management
- Implement Zustand stores with:
  - Multiple stores for different domains (tasks, menu, user)
  - Middleware (persist, devtools)
  - Async actions
  - Computed/derived state
- Use Context API where appropriate (theme, auth context)
- Choose the right tool for each use case

#### 3. Advanced Routing
- Implement nested routes:
  - `/dashboard` → Main layout
  - `/dashboard/tasks` → Tasks page
  - `/dashboard/menu` → Menu page
  - `/dashboard/settings` → Settings page
- Create protected routes (require authentication)
- Implement route-based code splitting with `React.lazy`
- Add error boundaries for route-level error handling
- Use route loaders for data prefetching (optional)

#### 4. Task Management Module
- Full CRUD operations (Create, Read, Update, Delete)
- Task persistence using `localStorage` or API
- Form handling with React Hook Form
- Form validation with TypeScript
- Derived state: completed counts, overdue flags, statistics
- Filtering and sorting tasks

#### 5. Menu Module
- Consume TheMealDB API with proper error handling
- Implement loading states and skeletons
- Add caching strategy to avoid unnecessary API calls
- Handle race conditions in API calls
- Implement optimistic updates for favorites
- Error recovery and retry logic

#### 6. Performance Optimization
- Use `React.memo` for expensive components
- Implement `useMemo` for expensive calculations
- Use `useCallback` for stable function references
- Code splitting with `React.lazy` and `Suspense`
- Optimize bundle size
- Profile with React DevTools Profiler
- Document performance improvements

#### 7. Error Handling
- Implement error boundaries at route level
- User-friendly error messages
- Error logging (console or service)
- Recovery strategies (retry buttons, fallback UI)
- Handle API errors gracefully

#### 8. Testing
- Set up Jest and React Testing Library
- Write tests for:
  - Critical components (TaskList, MenuCard)
  - Custom hooks
  - Utility functions
  - User interactions (clicks, form submissions)
- Mock API calls in tests
- Achieve at least 60% test coverage for core features

#### 9. Deployment
- Optimize production build
- Set up environment variables
- Deploy to Vercel or Render
- Configure custom domain (optional)
- Set up CI/CD pipeline (GitHub Actions optional)
- Create deployment documentation

### Application Structure

```
src/
├── components/
│   ├── Dashboard/
│   │   ├── DashboardLayout.tsx
│   │   └── DashboardNav.tsx
│   ├── Tasks/
│   │   ├── TaskList.tsx
│   │   ├── TaskForm.tsx
│   │   ├── TaskCard.tsx
│   │   └── TaskStats.tsx
│   ├── Menu/
│   │   ├── MenuGrid.tsx
│   │   ├── MenuCard.tsx
│   │   └── MenuFilters.tsx
│   └── ErrorBoundary.tsx
├── hooks/
│   ├── useLocalStorage.ts
│   ├── useFetch.ts
│   └── useDebounce.ts
├── stores/
│   ├── taskStore.ts
│   ├── menuStore.ts
│   └── userStore.ts
├── pages/
│   ├── DashboardPage.tsx
│   ├── TasksPage.tsx
│   ├── MenuPage.tsx
│   └── SettingsPage.tsx
├── services/
│   └── api.ts
├── types/
│   ├── task.types.ts
│   └── menu.types.ts
└── __tests__/
    ├── components/
    └── hooks/
```

## Daily Breakdown

### Day 11: Task Management & Forms
- Build task management module with CRUD operations
- Implement React Hook Form for task creation/editing
- Create `useLocalStorage` custom hook
- Add form validation

**Deliverable:** Fully functional task management with forms

### Day 12: API Integration & Effects
- Build menu module with TheMealDB API
- Implement `useEffect` for data fetching
- Add loading states and error handling
- Create `useFetch` custom hook
- Implement caching strategy

**Deliverable:** Menu module with robust API integration

### Day 13: Advanced Routing & Error Handling
- Set up nested routes
- Implement protected routes
- Add route-based code splitting
- Create error boundaries
- Implement error handling patterns

**Deliverable:** Multi-page dashboard with advanced routing

### Day 14: Performance & Testing
- Optimize components with React.memo, useMemo, useCallback
- Implement code splitting
- Profile application with React DevTools
- Write tests for critical components
- Document performance improvements

**Deliverable:** Optimized and tested application

### Day 15: Deployment & Presentation
- Prepare production build
- Set up environment variables
- Deploy to Vercel or Render
- Create deployment documentation
- Prepare demo presentation

**Deliverable:** Live deployed application and presentation

## Systems Drill: Deployment Checklist

Create a comprehensive `deploy-checklist.md` covering:

### Pre-Deployment
- [ ] All tests passing
- [ ] Build succeeds without errors
- [ ] Environment variables documented
- [ ] Performance audit completed
- [ ] Error boundaries tested
- [ ] Responsive design verified

### Deployment Steps
- [ ] Repository connected to deployment platform
- [ ] Environment variables configured
- [ ] Build command verified
- [ ] Deploy and verify build logs
- [ ] Smoke test all major features
- [ ] Verify API endpoints work
- [ ] Check error handling

### Post-Deployment
- [ ] Monitor error logs
- [ ] Verify analytics (if added)
- [ ] Test on multiple devices
- [ ] Document deployment process
- [ ] Create rollback plan

## Stretch Ideas
- Add authentication (mock or real)
- Implement React Query or SWR for advanced data fetching
- Add dark mode with theme persistence
- Create admin panel with protected routes
- Add real-time updates (WebSockets or polling)
- Implement PWA features (service workers, offline support)
- Add analytics tracking
- Create component library documentation with Storybook

## Deliverables
- **Complete "Krusty Krab Dashboard"** application with all features
- **Repo structure:** All code in the same repository, organized by feature branches
- **Git Flow workflow:** Final release via `release/*` branch merged to `main` (see [Git Flow guide](../../guides/gitflow-workflow.md))
- **Testing:** At least 60% test coverage for core features
- **Documentation:**
  - Comprehensive README with setup, architecture, and deployment
  - `deploy-checklist.md` with deployment steps
  - Code comments for complex logic
- **Deployment:**
  - Live application on Vercel or Render
  - Environment variables properly configured
  - Production build optimized
- **Demo Presentation:**
  - 5-10 minute presentation
  - Feature walkthrough
  - Technical highlights
  - Lessons learned

## Reference Materials
- React docs: `https://react.dev/learn` (Effects, Custom Hooks, Performance)
- React Router docs: `https://reactrouter.com/en/main` (Advanced patterns)
- Zustand docs: `https://docs.pmnd.rs/zustand` (Advanced patterns, middleware)
- React Hook Form: `https://react-hook-form.com/`
- React Testing Library: `https://testing-library.com/react`
- Vercel Deployment: `https://vercel.com/docs`
- Render Deployment: `https://render.com/docs`
- Internal assets: [`gitflow-workflow.md`](../../guides/gitflow-workflow.md), [`deploy-checklist-template.md`](assets/deploy-checklist-template.md), [`dashboard-data-flow.md`](assets/dashboard-data-flow.md)

---

**Navigation:** [Stage 3 Overview](topics.md) · [Stage 2: State & Styling](../2/topics.md) · [Program Overview](../../README.md)
