# 🦑 SpongeBob React Bootcamp: 3-Week Underwater Training Ship for Engineers

<p align="center">
  <img src="https://cdn.gamma.app/4my05amn4b2pizt/generated-images/kspclTOQYOkQjnuYEvrOH.png" alt="SpongeBob React Bootcamp course diagram" style="max-width: 600px; width: 100%; border-radius: 12px; box-shadow: 0 4px 14px #0001;" />
</p>

**Theme:** "Learn React under the sea — guided by SpongeBob, Patrick, and Sandy!".

This intensive, fast-paced training voyage is **React-focused from day one**. The program runs for approximately **3 weeks** (15 sessions, 2–3 hours each), following an intensive and playful style (SpongeBob energy + developer focus). All work is tracked in a single GitHub repository following professional Git workflows.


## 🏁 Mission & Goals
By the end of this training, every SpongeBob-in-training will achieve the following milestones:
1.  **Understand how to build interactive web apps using React**.
2.  Be comfortable with **modern JavaScript (ES6+)**.
3.  **Complete and deploy a small React app** (“Krusty Krab Dashboard”).
4.  Work like a real developer, utilizing **Git, code reviews, and mini-sprints**.

**The continuous Learning Loop:** Learn → Code → Build → Show → Reflect.

## ✅ Prerequisites & Setup

Before starting the bootcamp, ensure you have the following tools and technologies set up:

### Tooling

- **VS Code** with recommended extensions:
  - Biome (replaces ESLint + Prettier)
  - Live Server (for vanilla JS development and experiments)
  - Auto Rename Tag (optional but helpful)
  - TypeScript and JavaScript Language Features (built-in)
- **Node.js (latest LTS) via NVM**  
  ```bash
  nvm install --lts && nvm use --lts
  ```
- **Git** (CLI) with GitHub or GitLab access and SSH keys configured
- **Git Flow workflow**: All work must be submitted via feature branches and pull/merge requests. See the [Git Flow Workflow Guide](guides/gitflow-workflow.md) for detailed instructions.
- **Commitlint**: Commit messages must follow [Conventional Commits](https://www.conventionalcommits.org/) format (enforced via [commitlint](https://github.com/conventional-changelog/commitlint))
- **Package manager**: `npm` (bundled with Node.js) or `pnpm` if preferred
- **Browser DevTools-ready browser** (Chrome, Edge, or Firefox)
- **Optional helpers**: Postman or Bruno for API exploration

### Technologies & Libraries

Throughout the bootcamp, you'll work with:

- **TypeScript** - All React projects use TypeScript for type safety and better developer experience
- **React with TypeScript** (function components, hooks, routing, type definitions)
- **State Management** with **Zustand**
- **Form Handling** via **React Hook Form**
- **HTTP/REST Client**: **Axios**
- **Git Workflow**: **Git Flow** (feature branches, develop/main branches, PR reviews) + **lefthook** (Git hook manager) + **commitlint** (commit message linting)
- **Code Quality & Formatting**: **Biome.js** (linting + formatting)
- **Testing**: Jest + React Testing Library (intro level)
- **Styling Options**: Tailwind CSS or CSS Modules (based on cohort preference)
- **Deployment Targets**: Render and Vercel
- **API Integrations**: TheMealDB (primary), plus mock APIs for exercises

> **📚 Guides & Documentation:** For detailed guides on workflows and best practices, check the [`guides/`](guides/) folder, including the comprehensive [Git Flow Workflow Guide](guides/gitflow-workflow.md).

## 📦 Assets & Templates

- **Guides**: See the [`guides/`](guides/) folder for detailed documentation:
  - [`gitflow-workflow.md`](guides/gitflow-workflow.md) - Complete guide for feature branches, PRs, and code review process
- **Stage 0** (Optional): [`mealdb-endpoints.md`](stages/0/assets/mealdb-endpoints.md), [`favorites-schema.json`](stages/0/assets/favorites-schema.json) - Vanilla JS resources
- **Stage 1**: [`react-setup-guide.md`](stages/1/assets/react-setup-guide.md), [`component-examples.md`](stages/1/assets/component-examples.md) - React setup and component examples
- **Stage 2**: [`menu-board-wireframe.md`](stages/2/assets/menu-board-wireframe.md), [`resident-card-contract.md`](stages/2/assets/resident-card-contract.md)
- **Stage 3**: [`deploy-checklist-template.md`](stages/3/assets/deploy-checklist-template.md), [`dashboard-data-flow.md`](stages/3/assets/dashboard-data-flow.md)

---

## 🌊 Program Stages

The curriculum is structured in **4 stages** (1 optional + 3 core), designed to take you from JavaScript basics to deploying production-ready React applications. All work is tracked in a single GitHub repository using professional Git workflows.

| Stage | Focus | Duration | Key Deliverable |
|:---|:---|:---|:---|
| **🪸 Stage 0** (Optional) | Vanilla JavaScript Foundation | 5 days | "Krusty Krab Orders" - Vanilla JS app |
| **🌊 Stage 1** | React Basics & Environment Setup | 5 days | "Interactive Welcome Board" - First React app |
| **🌴 Stage 2** | State, Styling & Advanced Components | 5 days | "Krusty Menu Board" - Full-featured React app |
| **⚓ Stage 3** | Advanced Patterns & Deployment | 5 days | "Krusty Krab Dashboard" - Production-ready app |

> **💡 Pro Tip:** If you're already comfortable with JavaScript, you can skip Stage 0 and jump straight into React with Stage 1!

### 🪸 STAGE 0 — "Vanilla JavaScript Foundation" (Optional Pre-Stage)

[Stage Overview](stages/0/topics.md) · [Task Brief](stages/0/tasks.md)

**Goal:** Build a strong base in modern JavaScript for complete beginners before diving into React.

| Focus Area | Key Concepts | Milestone |
| :--- | :--- | :--- |
| **Vanilla JS Mastery** | HTML & CSS refresher, JS basics, and **ES6+ features** (arrow functions, destructuring, promises). | Functional **"Krusty Krab Orders" app built with vanilla JS**. |
| **Interactivity & Data** | **DOM manipulation & event handling**. Using the **Fetch API + async/await** with TheMealDB. | |

> **Note:** This stage is optional. If you already have JavaScript experience, you can skip directly to Stage 1.

### 🌊 STAGE 1 — "Welcome to Bikini Bottom: React Basics & Environment Setup"

[Stage Overview](stages/1/topics.md) · [Task Brief](stages/1/tasks.md)

**Goal:** Set up a professional development environment and learn React fundamentals from day one.

| Focus Area | Key Concepts | Milestone |
| :--- | :--- | :--- |
| **Environment Setup** | **NVM, Node.js, VS Code configuration**, **GitHub repository creation**, **Vite + React + TypeScript** project initialization, **Git Flow workflow** setup. | Fully configured development environment with working React + TypeScript project. |
| **React Fundamentals** | **JSX syntax**, **React components** (function components), **TypeScript basics** (interfaces, types), **component composition**, and **project structure**. | **"Interactive Welcome Board"** built with React components, TypeScript types, and proper Git workflow. |

### 🌴 STAGE 2 — "React Lagoon: State, Styling, and Advanced Components"

[Stage Overview](stages/2/topics.md) · [Task Brief](stages/2/tasks.md)

**Goal:** Deep dive into React's core concepts: state management, styling, routing, and debugging tools.

| Focus Area | Key Concepts | Milestone |
| :--- | :--- | :--- |
| **State & Data** | **useState hook**, **Virtual DOM** understanding, **array operations** (filter, map, reduce), **Zustand** state management, **Context API**, and **React DevTools** debugging. | **"Krusty Menu Board"** app with state management, filtering, and routing. |
| **Styling & Layout** | **SCSS/SASS**, **Flexbox** layouts, element positioning, **Tailwind CSS**, responsive design, and component styling patterns. | |
| **Routing & Architecture** | **React Router** v6, client-side routing, navigation patterns, **props deep dive**, and component composition. | |

### ⚓ STAGE 3 — "Sail to the Surface: Advanced Hooks, Patterns, and Deployment"

[Stage Overview](stages/3/topics.md) · [Task Brief](stages/3/tasks.md)

**Goal:** Master advanced React patterns, optimize performance, and deploy a production-ready application.

| Focus Area | Key Concepts | Milestone (Capstone) |
| :--- | :--- | :--- |
| **Advanced Patterns** | **useEffect** hook mastery, **custom hooks**, **advanced routing** (nested routes, protected routes), **performance optimization** (React.memo, useMemo, useCallback), **error boundaries**, and **testing** with Jest & React Testing Library. | **Build and deploy "Krusty Krab Dashboard,"** a production-ready management app with advanced patterns, performance optimizations, and full test coverage. |
| **Production Ready** | **React Hook Form** for forms, **advanced Zustand** patterns, **API integration** with error handling, **code splitting**, and **deployment** to Vercel/Render with CI/CD. | On Demo Day, trainees present their live app and earn the **Golden Spatula of React 🥇**. |

***