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

## 🚀 Advanced Challenges (For Experienced Students)

If you find the core assignment too easy, here are more challenging tasks that will push your React and TypeScript skills further:

### Advanced Component Patterns
- **Compound Components**: Build a `ResidentCard` using the compound component pattern (e.g., `ResidentCard.Header`, `ResidentCard.Body`, `ResidentCard.Footer`)
- **Render Props Pattern**: Create a reusable `DataFetcher` component that uses render props to handle data fetching logic
- **Higher-Order Components (HOCs)**: Build an HOC that adds loading states or error boundaries to any component
- **Polymorphic Components**: Create a `Box` component that can render as different HTML elements (`div`, `section`, `article`) based on props

### Advanced TypeScript
- **Generic Components**: Build a generic `List<T>` component that works with any data type
- **Discriminated Unions**: Use TypeScript discriminated unions for complex prop types (e.g., different card variants)
- **Utility Types**: Leverage TypeScript utility types (`Partial`, `Pick`, `Omit`, `Record`) for component props
- **Type Guards**: Implement runtime type checking with TypeScript type guards

### Development Tooling
- **Storybook Setup**: Set up Storybook and document all components with stories, controls, and documentation
- **Component Testing**: Write unit tests for components using Vitest (Vite's test runner) and React Testing Library
- **CI/CD Basics**: Set up GitHub Actions to run tests and linting on every PR
- **Pre-commit Hooks**: Configure Husky or lefthook with pre-commit hooks for linting and type checking

### Advanced Project Structure
- **Monorepo Setup**: Organize the project as a monorepo with separate packages for components and utilities
- **Path Aliases**: Configure TypeScript path aliases (`@/components`, `@/utils`) for cleaner imports
- **Barrel Exports**: Create index files for clean component exports
- **Design System Foundation**: Build a basic design system with tokens (colors, spacing, typography)

### Performance & Best Practices
- **Code Splitting**: Implement route-based code splitting even at this early stage
- **Lazy Loading**: Use `React.lazy` and `Suspense` for component lazy loading
- **Memoization**: Practice with `React.memo` to prevent unnecessary re-renders
- **Bundle Analysis**: Use tools like `vite-bundle-visualizer` to analyze bundle size

### Advanced Git Workflow
- **Conventional Commits Automation**: Set up automated changelog generation from commit messages
- **Branch Protection Rules**: Configure branch protection rules on GitHub
- **PR Templates**: Create pull request templates with checklists and guidelines
- **Semantic Versioning**: Implement semantic versioning for releases

**Deliverable for Advanced Challenges:**
- Complete at least 3 of the above challenges
- Document your approach and decisions in the README
- Create a separate PR for each advanced feature
- Include tests or Storybook stories for your advanced components

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
