### ⚓ STAGE 3: "Sail to the Surface: State Architecture, Routing & Delivery"

#### I. Goal and Focus
Stage 3 emphasizes production-ready state architecture, enterprise routing, validated forms, portal/overlay systems, tasteful animations, automated testing, and CI/CD/security discipline. Trainees will design resilient stores, ship guarded navigation flows, validate data with React Hook Form + Zod, orchestrate overlays + animations, implement CSP/security headers, and deploy confidently.

#### II. Key Topics (Lecture/Instructional Material)
The curriculum covers advanced React concepts and production-ready development:

| Topic Category | Specific Concepts Covered |
| :--- | :--- |
| **Advanced State Management** | Multi-store Zustand, middleware (persist, devtools, subscribeWithSelector), async actions, optimistic updates, computed selectors, Context API composition, state diagrams, data-flow governance. |
| **Advanced Routing** | Nested dashboards, protected routes, redirects, route metadata, error boundaries, `React.lazy` + `Suspense` splitting, data prefetch/loaders, and deep-link strategies. |
| **Form Management & Validation** | React Hook Form architecture, controller patterns, reusable field primitives, Zod schemas + inference, async validation, accessibility, draft persistence, and UX polish. |
| **Data Fetching & Domain Logic** | API integration with caching and retry, TheMealDB module, race-condition handling, optimistic mutations, and sync between stores and network sources. |
| **Testing Strategy** | Jest + React Testing Library for units/components, component-driven tests, Playwright or Cypress E2E flows, coverage tracking, mocking APIs/stores, CI gating. |
| **CI/CD & Deployment** | GitHub Actions stages, preview + production workflows, environment management, rollout/rollback plans, monitoring hooks, deployment documentation, and demo readiness. |
| **Professional Patterns** | Component composition, render props/HOCs where necessary, feature-flag driven UX, and documentation practices for handoff. |
| **Portal & Overlay Systems** | Centralized portal manager, focus trapping, accessibility, routing-aware overlays, and comparing custom UX with the native `<dialog>` element. |
| **Animation Foundations** | CSS transitions/animations, Motion (`motion.dev`) + ReactBits recipes, performance considerations (`will-change`, GPU transforms), and graceful fallbacks. |
| **Security (CSP & Headers)** | Authoring CSP policies, configuring security headers on Vercel/Render, handling third-party scripts, and testing enforcement locally + in CI. |

#### III. Daily Challenges (Practice/Application)
Trainees build the capstone project integrating all advanced concepts:

| Days | Practice Project | Skill Focus |
| :--- | :--- | :--- |
| **Day 11** | **"State Architecture Lab"** | Design multi-store Zustand/Context graph, selectors, middleware, and documentation for data flow. |
| **Day 12** | **"Routing System Workshop"** | Implement nested/parallel routes, protected flows, layout shells, portal/overlay manager, and error boundaries with code splitting. |
| **Day 13** | **"Validated Feature Delivery"** | Wire task/menu feature forms with React Hook Form + Zod, persistence, optimistic workflows, caching, plus CSS vs Motion/ReactBits animation exercises. |
| **Day 14** | **"Testing & Automation Lab"** | Build Jest/RTL suites plus Playwright/Cypress E2E coverage, integrate reports, and enforce CI gates. |
| **Day 15** | **"CI/CD & Demo"** | Finalize GitHub Actions pipeline, implement CSP/security headers, ship to Vercel/Render, document rollout/rollback plans, and prep demos. |

#### IV. Final Capstone & Milestone
The culmination of the entire program is the **Final Capstone** project:

**Project Name:** **"Krusty Krab Dashboard"**

**Description:** A production-ready management dashboard featuring:
- Multi-page experience with advanced routing and guarded layouts
- Task management with persistent Zustand stores
- Menu module with API integration, caching, and optimistic updates
- Form handling powered by React Hook Form + Zod validation
- Portal + overlay system with focus management and `<dialog>` comparisons
- Animation patterns delivered via CSS primitives and Motion/ReactBits snippets
- Automated testing stack (unit, component, E2E) captured in CI
- GitHub Actions pipeline plus Vercel/Render deployment
- CSP and security headers configured + documented
- Error boundaries, recovery flows, and documented rollout plans
- Responsive design with Tailwind CSS
- Deployed to production

**Milestone:** The application must be:
- ✅ Fully functional with all features implemented
- ✅ State architecture + routing flows documented
- ✅ Tested (≥70% unit/component coverage + passing Playwright/Cypress suite; BUT of course coverage doesn't mean app is functioning correctly, so just focust on most important modules)
- ✅ CI/CD pipeline green (lint, test, build, deploy)
- ✅ **Successfully deployed** to Vercel or Render
- ✅ Documented with README, ADRs, and deployment guide

The program concludes with a **Demo Day**, where **each trainee presents their live app** and earns the **Golden Spatula of React 🥇**.

---

**Resources:** [Stage 3 Task Brief](tasks.md) · [Stage 2: State & Styling](../2/topics.md) · [Program Overview](../../README.md)
