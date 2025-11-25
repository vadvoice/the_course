# Stage 3 Task Brief — State Architecture, Routing, Forms, and Delivery

## Core Assignment: "Krusty Krab Dashboard" (5-day capstone)

Build a production-ready management dashboard that demonstrates mastery of all React concepts learned throughout the bootcamp.

### Requirements

#### 1. Advanced State Management Architecture
- Design multi-store Zustand architecture (tasks, menu, user, layout) with clear domain boundaries
- Combine middleware (`persist`, `devtools`, `subscribeWithSelector`) for insight and persistence
- Implement async actions, optimistic updates, and error channels inside stores
- Derive computed state (statistics, filters, permissions) with memoized selectors
- Use Context API to expose global concerns (theme, auth, feature flags) and bridge stores into components
- Document state diagrams and data-flow decisions for handoff clarity

#### 2. Advanced Routing & Layout System
- Build nested dashboard layouts with shared shells (`/dashboard`, `/dashboard/tasks`, `/dashboard/menu`, `/dashboard/settings`)
- Implement protected routes with redirect flows, session checks, and loading fallbacks
- Apply route-level code splitting using `React.lazy` + `Suspense` with skeleton states
- Add error boundaries per route segment plus recovery UIs
- Prefetch critical data with loader-style utilities or manual warm-up functions
- Support deep-linking, programmatic navigation, and route metadata (breadcrumbs, titles)

#### 3. Form Management & Validation (React Hook Form + Zod)
- Use React Hook Form for all CRUD interactions (tasks, settings, menu filters)
- Define Zod schemas for every form, infer TypeScript types, and enforce validation messages
- Handle async validation (IDs, unique slugs) and server-side error surfaces
- Create reusable form primitives (Field, ErrorMessage) plus custom hooks (`useTaskForm`, `useSettingsForm`)
- Ensure accessibility (labels, aria attributes) and keyboard navigation across forms
- Persist drafts via Zustand/localStorage when users navigate away mid-edit

#### 4. Portal & Overlay Systems
- Design a centralized portal manager for modals, drawers, tooltips, and contextual menus
- Enforce focus trapping, keyboard navigation, aria attributes, and inert backgrounds
- Coordinate overlay lifecycles with routing (e.g., close on navigation, deep-link modals)
- Compare custom portal UX with the native `<dialog>` element, documenting tradeoffs
- Provide escape hatches for server-side rendering and nested portals

#### 5. Task Management Module
- Full CRUD operations (Create, Read, Update, Delete)
- Task persistence using `localStorage` or API
- Form handling with React Hook Form
- Form validation with TypeScript
- Derived state: completed counts, overdue flags, statistics
- Filtering and sorting tasks

#### 6. Menu Module
- Consume TheMealDB API with proper error handling
- Implement loading states and skeletons
- Add caching strategy to avoid unnecessary API calls
- Handle race conditions in API calls
- Implement optimistic updates for favorites
- Error recovery and retry logic

#### 7. Animation System Overview
- Deliver a quick-reference guide to CSS transitions/animations (utility classes, Tailwind helpers, or custom styles)
- Showcase how to reach for production-ready libraries like Motion (`https://motion.dev/`) or ReactBits (`https://www.reactbits.dev/`) when native CSS is insufficient
- Demonstrate at least one animated interaction (menu open, stats counter, progress indicator) using both pure CSS and a library abstraction
- Explain performance considerations (`will-change`, GPU-friendly transforms) and graceful degradation

#### 8. Automated Testing Stack
- Use Jest + React Testing Library for unit and component specs (stores, hooks, forms, routing guards)
- Add component-driven tests (Storybook or RTL) for dashboard widgets and error states
- Implement Playwright or Cypress E2E flows covering auth, routing, CRUD, and deployment smoke tests
- Mock APIs, Zustand stores, and timers predictably; isolate network behavior per suite
- Gate pull requests on unit + component suites; run E2E nightly or on-demand
- Target ≥70% coverage on core domains and document gaps with mitigation notes

#### 9. CI/CD & Deployment Automation
- Configure GitHub Actions (or similar) with stages for lint → test → build → E2E → deploy
- Provision environment variables securely for preview and production deployments
- Deploy to Vercel or Render with previews per PR and protected production branch releases
- Capture build artifacts, trace logs, and bundle metrics for troubleshooting
- Document rollback plans, release tagging strategy, and ownership for on-call/monitoring
- Ensure deployment docs describe setup, pipeline triggers, smoke procedures, and verification

#### 10. Frontend Security Hardening (CSP & Headers)
- Define a Content Security Policy tailored to the dashboard (script/style-src, connect-src) following modern guidance
- Configure security headers (`Strict-Transport-Security`, `X-Frame-Options`, `X-Content-Type-Options`, `Referrer-Policy`) in the deployment platform
- Document how CSP interacts with inline scripts/styles, third-party analytics, and asset hosting
- Add automated checks or CI reminders to keep the policy up to date (refer to Ignatovich’s CSP primer)

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

### Day 11: State Architecture & Domain Stores
- Model Zustand stores, selectors, and middleware for each domain
- Wire Context providers and data-flow diagrams
- Implement initial task/menu/user slices with mock data

**Deliverable:** Multi-store state layer with documentation and Storybook/Playground examples

### Day 12: Routing System & Layout Shells
- Build dashboard layout, nested routes, and navigation scaffolding
- Add protected routes, redirects, and loading boundaries
- Integrate route-level code splitting and error boundaries
- Implement the portal/overlay manager, ensuring focus traps and `<dialog>` comparisons

**Deliverable:** Fully navigable dashboard with guarded routes and fallbacks

### Day 13: Feature Forms & Validation
- Implement task CRUD and settings forms with React Hook Form + Zod
- Connect forms to state layer with optimistic/rollback flows
- Finalize menu module with caching + mutation flows
- Prototype key animations twice: once with CSS utilities, once with Motion/ReactBits

**Deliverable:** Feature-complete tasks/menu experiences with validated forms

### Day 14: Testing & Automation Sprint
- Author Jest/RTL unit + component tests for stores, hooks, routing guards
- Add Playwright/Cypress E2E suite covering critical journeys
- Capture coverage reports and integrate into CI status checks

**Deliverable:** Automated test suite (unit + component + E2E) with ≥70% coverage

### Day 15: CI/CD & Demo Prep
- Finalize GitHub Actions (or chosen) pipeline, including E2E step
- Deploy to Vercel/Render (preview + production) and document rollout plan
- Implement and verify CSP + security headers in the target platform
- Rehearse demo and prepare release notes

**Deliverable:** Passing CI/CD pipeline, live deployment, and demo-ready narrative

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
- Add role-based workspaces with per-tenant Zustand stores and routing guards
- Introduce workflow automation (task approvals, escalations) via state machines
- Layer feature-flag driven navigation that reveals experimental routes
- Build dynamic form builders backed by Zod schema registries
- Enable WebSocket or SSE feeds that hydrate stores in real time
- Capture visual regression snapshots for key layouts via Chromatic or Loki

## 🚀 Advanced Challenges (For Experienced Students)

If you find the core assignment too easy, tackle deeper platform concerns:

### State & Data Orchestration
- Compose Zustand with XState or statecharts for complex lifecycle management
- Implement selective persistence with encryption, migrations, and cross-tab sync
- Build time-travel debugging or audit trails for store mutations
- Add pluggable data providers (REST, GraphQL, mocked) switchable at runtime

### Routing & Experience Architecture
- Experiment with micro-frontends or Module Federation for dashboard sections
- Implement parallel and deferred routes leveraging React Router v7 previews
- Build content-driven navigation (breadcrumbs, URL params) sourced from CMS/config
- Add intelligent prefetching using heuristics (hover, visibility, user roles)
- Architect layered portal/overlay systems with robust focus traps and `<dialog>` fallbacks
- Choreograph advanced animations that combine Motion + CSS techniques tied to route transitions

### Form Systems & Validation
- Generate form UIs dynamically from shared Zod schema catalogs
- Add undo/redo stacks for form interactions using history-aware stores
- Integrate file uploads, signature pads, or nested array fields with RHF
- Provide offline drafts with conflict resolution when re-syncing

### Testing & Quality Gates
- Run full TDD cycles for net-new features, including contract tests for APIs
- Add visual regression, accessibility (axe/jest-axe), and performance smoke tests
- Parallelize Playwright/Cypress suites across shards and record videos/traces
- Track coverage per domain and block merges that regress critical areas

### Delivery, Observability & Ops
- Expand CI/CD to include preview URLs, canary deploys, and release tagging
- Layer feature flags, kill switches, and experimentation frameworks
- Instrument monitoring with Sentry/PostHog + dashboards for KPIs
- Containerize the app (Docker) and script blue/green rollouts or multi-region deploys
- Automate CSP/security header verification for each environment (CI smoke + response audits)

**Deliverable for Advanced Challenges:**
- Ship at least 5 advanced upgrades (mix of state, routing, testing, delivery)
- Produce a technical deep-dive doc covering architecture choices + tradeoffs
- Hit ≥90% meaningful test coverage and document critical-path protections
- Enable monitoring/alerting plus detailed runbooks for incidents
- Publish a case study or internal blog and present findings to the cohort

## Deliverables
- **Complete "Krusty Krab Dashboard"** application with all features
- **Repo structure:** All code in the same repository, organized by feature branches
- **Git Flow workflow:** Final release via `release/*` branch merged to `main` (see [Git Flow guide](../../guides/gitflow-workflow.md))
- **Testing:** ≥70% coverage across unit + component suites, green Playwright/Cypress E2E runs recorded in CI
- **Documentation:**
  - Comprehensive README with setup, architecture, and deployment
  - `deploy-checklist.md` with deployment + rollback steps
  - Code comments and ADRs for complex logic/state decisions
- **CI/CD:** GitHub Actions (or equivalent) pipeline covering lint, tests, build, E2E, and deployment gates
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
- React docs: `https://react.dev/learn` (State management, context, concurrent rendering fundamentals)
- React Router docs: `https://reactrouter.com/en/main` (Nested layouts, data APIs, code splitting)
- Zustand docs: `https://docs.pmnd.rs/zustand` (Multi-store patterns, middleware)
- React Hook Form: `https://react-hook-form.com/`
- Zod: `https://zod.dev/`
- React Testing Library: `https://testing-library.com/react`
- Playwright: `https://playwright.dev/` / Cypress: `https://www.cypress.io/`
- Motion: `https://motion.dev/`
- ReactBits animation snippets: `https://www.reactbits.dev/`
- GitHub Actions: `https://docs.github.com/en/actions`
- Vercel Deployment: `https://vercel.com/docs`
- Render Deployment: `https://render.com/docs`
- CSP + security headers primer: `https://medium.com/@ignatovich.dm/building-secure-frontend-applications-with-content-security-policy-csp-2243322d4af1`
- Internal assets: [`gitflow-workflow.md`](../../guides/gitflow-workflow.md), [`deploy-checklist-template.md`](assets/deploy-checklist-template.md), [`dashboard-data-flow.md`](assets/dashboard-data-flow.md)

---

**Navigation:** [Stage 3 Overview](topics.md) · [Stage 2: State & Styling](../2/topics.md) · [Program Overview](../../README.md)
