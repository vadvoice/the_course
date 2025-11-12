# Stage 1 Task Brief — React Basics & Environment Setup

## Day 1: Environment Setup & Repository Creation

### Setup Tasks
1. **Install NVM (Node Version Manager)**
   - Follow installation guide for your OS
   - Verify installation: `nvm --version`

2. **Install Node.js (Latest LTS)**
   - Run: `nvm install --lts && nvm use --lts`
   - Verify: `node --version` and `npm --version`

3. **Configure VS Code**
   - Install recommended extensions:
     - Biome (linting + formatting)
     - TypeScript and JavaScript Language Features (built-in)
     - Auto Rename Tag
     - ESLint (if not using Biome)
   - Configure settings for TypeScript and React

4. **Create GitHub Repository**
   - Create a new repository: `spongebob-react-bootcamp` (or similar)
   - Initialize with README (optional)
   - Clone locally: `git clone <your-repo-url>`

5. **Initialize React + TypeScript Project**
   - Navigate to repo: `cd spongebob-react-bootcamp`
   - Create Vite project: `npm create vite@latest . -- --template react-ts`
   - Install dependencies: `npm install`
   - Test dev server: `npm run dev`

6. **Set Up Git Flow**
   - Create `develop` branch: `git checkout -b develop`
   - Push `develop` to remote: `git push -u origin develop`
   - Follow [Git Flow guide](../../guides/gitflow-workflow.md) for branch structure

7. **Configure Commitlint**
   - Install: `npm install --save-dev @commitlint/cli @commitlint/config-conventional`
   - Create `commitlint.config.js` (see guide)
   - Test with a commit message

### Deliverables
- ✅ Working development environment
- ✅ GitHub repository with `main` and `develop` branches
- ✅ React + TypeScript project running locally
- ✅ First commit following Conventional Commits format

## Days 2-5: React Fundamentals Practice

### Core Assignment: "Interactive Welcome Board"
Build a React application that displays information about Bikini Bottom residents with interactive elements.

**Requirements:**
- Create reusable `ResidentCard` component with TypeScript props
- Display at least 3 characters (SpongeBob, Patrick, Squidward)
- Use proper TypeScript interfaces for all props
- Implement basic interactivity (click to show/hide details, toggle favorite)
- Organize components in a clear folder structure
- Apply basic styling (CSS Modules or Tailwind)

### Component Structure
```
src/
├── components/
│   ├── ResidentCard.tsx
│   ├── WelcomeBoard.tsx
│   └── types.ts
├── App.tsx
└── main.tsx
```

### TypeScript Requirements
- Define interfaces for all component props
- Type all function parameters and return values
- Use proper typing for event handlers

### Git Workflow
- Create feature branch: `feature/stage1-welcome-board`
- Make commits following Conventional Commits
- Create PR to `develop` branch
- Get code review and merge

## Lab Drills (Practice Components)

### Day 2-3: Component Practice
- Create simple greeting components
- Practice JSX syntax and expressions
- Experiment with props and TypeScript

### Day 4: Composition Practice
- Build nested component structures
- Practice component composition patterns
- Work with static data arrays

## Stretch Ideas
- Add CSS animations for component interactions
- Create a theme provider component
- Implement a simple prop validation utility
- Add Storybook for component documentation

## Deliverables
- Repo structure: All code in the main repository, organized by feature branches
- **Git Flow workflow**: All code submitted via feature branches with pull/merge requests to `develop` branch (see [Git Flow guide](../../guides/gitflow-workflow.md))
- README.md with:
  - Project setup instructions
  - Development workflow
  - Component documentation
- At least 2 merged PRs demonstrating Git Flow workflow

## Reference Materials
- React docs: `https://react.dev/learn` (Start here: "Describing the UI")
- TypeScript Handbook: `https://www.typescriptlang.org/docs/handbook/intro.html` (focus on types, interfaces)
- React TypeScript Cheatsheet: `https://react-typescript-cheatsheet.netlify.app/`
- Vite documentation: `https://vitejs.dev/guide/`
- Internal assets: [`gitflow-workflow.md`](../../guides/gitflow-workflow.md), [`react-setup-guide.md`](assets/react-setup-guide.md), [`component-examples.md`](assets/component-examples.md)

---

**Navigation:** [Stage 1 Overview](topics.md) · [Stage 2: React Components & State](../2/topics.md) · [Program Overview](../../README.md)
