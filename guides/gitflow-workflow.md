# Git Flow Workflow Guide

All course work must follow the **Git Flow** branching model for code review and collaboration. This ensures professional development practices and prepares trainees for real-world team workflows.

## Overview

Git Flow uses two main branches:
- **`main`**: Production-ready code (official release history)
- **`develop`**: Integration branch for features (working development line)

Plus supporting branch types:
- **`feature/*`**: New features (branched from `develop`)
- **`release/*`**: Preparing releases (branched from `develop`)
- **`hotfix/*`**: Critical production fixes (branched from `main`)

## Initial Setup

### 1. Create the `develop` branch

```bash
git checkout main
git checkout -b develop
git push -u origin develop
```

### 2. Clone and track `develop` (for team members)

```bash
git clone <repository-url>
git checkout -b develop origin/develop
```

## Feature Branch Workflow

### Creating a Feature Branch

Always branch from `develop`:

```bash
git checkout develop
git pull origin develop
git checkout -b feature/week1-pantry-explorer
```

**Naming convention**: `feature/week1-pantry-explorer`, `feature/week2-menu-board`, etc.

### Working on a Feature

1. Make commits with clear messages:
   ```bash
   git add .
   git commit -m "feat: add ingredient search functionality"
   ```

2. Push your feature branch regularly:
   ```bash
   git push -u origin feature/week1-pantry-explorer
   ```

### Submitting for Review

1. **Create a Pull Request (GitHub) or Merge Request (GitLab)**
   - Source: `feature/your-feature-name`
   - Target: `develop`
   - Include a clear description of changes

2. **Wait for code review** from instructors/peers

3. **Address feedback** by pushing additional commits to the same branch

4. **After approval**, merge into `develop` (typically via the PR/MR interface)

### Finishing a Feature

After merging, clean up locally:

```bash
git checkout develop
git pull origin develop
git branch -d feature/week1-pantry-explorer
```

## Weekly Workflow Example

### Week 1: Krusty Pantry Explorer

```bash
# Start the week
git checkout develop
git pull origin develop
git checkout -b feature/week1-pantry-explorer

# Work and commit
git add .
git commit -m "feat: implement API search integration"
git push origin feature/week1-pantry-explorer

# Create PR: feature/week1-pantry-explorer → develop
# After review and merge, continue with next feature or lab
```

### Week 2: Menu Board

```bash
git checkout develop
git pull origin develop
git checkout -b feature/week2-menu-board
# ... work and PR process
```

### Week 3: Dashboard Capstone

```bash
git checkout develop
git pull origin develop
git checkout -b feature/week3-dashboard
# ... work and PR process
```

## Release Process (Week 3 Final)

When ready to deploy the capstone:

```bash
git checkout develop
git checkout -b release/v1.0.0
# Final polish, bug fixes, documentation
# Create PR: release/v1.0.0 → main
# After merge, tag the release
git checkout main
git tag -a v1.0.0 -m "Release: Krusty Krab Dashboard v1.0.0"
git push origin v1.0.0
```

## Commit Message Guidelines

All commit messages must follow the **Conventional Commits** format and will be validated by [commitlint](https://github.com/conventional-changelog/commitlint).

### Format

```
type(scope?): subject
```

- **type** (required): The type of change
- **scope** (optional): The area of the codebase affected
- **subject** (required): Brief description of the change

### Commit Types

Based on [commitlint-config-conventional](https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/config-conventional):

- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation changes
- `style:` - Code style changes (formatting, missing semicolons, etc.)
- `refactor:` - Code refactoring (neither a bug fix nor a feature)
- `perf:` - Performance improvements
- `test:` - Adding or updating tests
- `build:` - Build system or external dependencies
- `ci:` - CI/CD configuration changes
- `chore:` - Maintenance tasks (dependencies, tooling)
- `revert:` - Revert a previous commit

### Examples

```bash
feat: add favorites persistence with localStorage
feat(api): integrate TheMealDB search endpoint
fix: handle API error states gracefully
fix(ui): correct button alignment on mobile
docs: update README with deployment steps
docs(api): add JSDoc comments to fetch functions
style: format code with Biome
refactor: extract search logic into separate module
test: add unit tests for favorite toggle
chore: update dependencies
chore(deps): bump axios to latest version
```

### Scope Examples

Scopes help identify which part of the codebase is affected:

```bash
feat(api): add ingredient search
fix(ui): resolve menu card overflow
docs(readme): update setup instructions
refactor(components): simplify MenuCard props
test(utils): add tests for localStorage helpers
```

### Setup commitlint

Projects should include commitlint configuration. Example setup:

```bash
npm install --save-dev @commitlint/cli @commitlint/config-conventional
```

Create `commitlint.config.js`:

```javascript
export default {
  extends: ['@commitlint/config-conventional'],
};
```

With **lefthook**, commitlint can be automatically enforced on commit hooks.

## Best Practices

1. **Always start from `develop`** when creating feature branches
2. **Keep features small and focused** - one feature per branch
3. **Pull latest `develop`** before creating new branches
4. **Write descriptive PR/MR descriptions** explaining what and why
5. **Review your own PR** before requesting review
6. **Respond to feedback promptly** and professionally
7. **Never force push** to shared branches (`main`, `develop`)

## Troubleshooting

### Merge conflicts with `develop`

```bash
git checkout feature/your-feature
git fetch origin
git merge origin/develop
# Resolve conflicts, then:
git add .
git commit -m "chore: resolve merge conflicts with develop"
git push origin feature/your-feature
```

### Need to update your feature branch

```bash
git checkout feature/your-feature
git pull origin develop
# Resolve any conflicts, then push
git push origin feature/your-feature
```

## Reference

- [Atlassian Git Flow Tutorial](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [commitlint Documentation](https://github.com/conventional-changelog/commitlint) - Commit message linting
- [Conventional Commits Specification](https://www.conventionalcommits.org/) - Commit message format standard
- GitHub: [Creating a Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
- GitLab: [Creating a Merge Request](https://docs.gitlab.com/ee/user/project/merge_requests/creating_merge_requests.html)

---

**Navigation:** [Pre-Requirements](../pre-requirements.md) · [Program Overview](../README.md)

