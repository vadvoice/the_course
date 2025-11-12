# React + TypeScript Setup Guide

This guide walks through setting up a professional React development environment for Stage 1.

## Prerequisites Checklist

- [ ] NVM installed and working
- [ ] Node.js (LTS) installed via NVM
- [ ] VS Code installed with recommended extensions
- [ ] Git installed and configured
- [ ] GitHub account with SSH keys set up

## Step-by-Step Setup

### 1. Install NVM (Node Version Manager)

**macOS/Linux:**
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
```

**Windows:**
Download and run the installer from: https://github.com/coreybutler/nvm-windows/releases

**Verify installation:**
```bash
nvm --version
```

### 2. Install Node.js (Latest LTS)

```bash
# Install latest LTS version
nvm install --lts

# Use the LTS version
nvm use --lts

# Verify installation
node --version  # Should show v20.x.x or similar
npm --version   # Should show 10.x.x or similar

# Set as default (optional)
nvm alias default node
```

### 3. Configure VS Code

**Install Extensions:**
1. Open VS Code
2. Go to Extensions (Cmd+Shift+X / Ctrl+Shift+X)
3. Install:
   - **Biome** (by biomejs) - Linting and formatting
   - **TypeScript and JavaScript Language Features** (built-in)
   - **Auto Rename Tag** (by Jun Han) - Helpful for JSX
   - **ESLint** (optional, if not using Biome)

**Recommended VS Code Settings:**
Create or update `.vscode/settings.json`:
```json
{
  "editor.defaultFormatter": "biomejs.biome",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "quickfix.biome": "explicit",
    "source.organizeImports.biome": "explicit"
  },
  "typescript.tsdk": "node_modules/typescript/lib",
  "typescript.enablePromptUseWorkspaceTsdk": true
}
```

### 4. Create GitHub Repository

1. Go to GitHub and create a new repository
   - Name: `spongebob-react-bootcamp` (or your preferred name)
   - Description: "React Bootcamp - Learning React with SpongeBob theme"
   - Visibility: Public or Private (your choice)
   - **Do NOT** initialize with README, .gitignore, or license (we'll do this locally)

2. Clone the repository:
```bash
git clone git@github.com:YOUR_USERNAME/spongebob-react-bootcamp.git
cd spongebob-react-bootcamp
```

### 5. Initialize Vite + React + TypeScript Project

```bash
# Create Vite project in current directory
npm create vite@latest . -- --template react-ts

# Install dependencies
npm install

# Start development server
npm run dev
```

**Verify it works:**
- Open `http://localhost:5173` in your browser
- You should see the Vite + React welcome page

### 6. Set Up Git Flow

```bash
# Create develop branch
git checkout -b develop

# Push develop to remote
git push -u origin develop

# Switch back to main (optional, for reference)
git checkout main
```

**Branch Structure:**
- `main` - Production-ready code
- `develop` - Integration branch for features
- `feature/*` - Feature branches (created from `develop`)

### 7. Configure Commitlint

```bash
# Install commitlint
npm install --save-dev @commitlint/cli @commitlint/config-conventional
```

Create `commitlint.config.js` in project root:
```javascript
export default {
  extends: ['@commitlint/config-conventional'],
};
```

**Test it:**
```bash
# This should pass
echo "feat: add initial setup" | npx commitlint

# This should fail
echo "bad commit message" | npx commitlint
```

### 8. Initial Commit

```bash
# Stage all files
git add .

# Make first commit (following Conventional Commits)
git commit -m "chore: initial project setup with Vite + React + TypeScript"

# Push to develop
git checkout develop
git push origin develop
```

## Project Structure

After setup, your project should look like:

```
spongebob-react-bootcamp/
├── .vscode/
│   └── settings.json
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   ├── App.tsx
│   ├── main.tsx
│   └── vite-env.d.ts
├── .gitignore
├── commitlint.config.js
├── index.html
├── package.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
```

## Next Steps

1. Create your first feature branch: `git checkout -b feature/stage1-welcome-board`
2. Start building components following the [Component Examples](component-examples.md)
3. Make commits following Conventional Commits format
4. Create PRs to `develop` branch

## Troubleshooting

**NVM not found after installation:**
- Close and reopen terminal
- Or run: `source ~/.bashrc` (Linux) or `source ~/.zshrc` (macOS)

**Vite dev server not starting:**
- Check Node version: `node --version` (should be 18+)
- Clear cache: `rm -rf node_modules package-lock.json && npm install`

**TypeScript errors:**
- Restart VS Code
- Check `tsconfig.json` is present
- Run: `npm run build` to see all TypeScript errors

---

**Related Task:** [Stage 1 Task Brief](../../tasks.md)

