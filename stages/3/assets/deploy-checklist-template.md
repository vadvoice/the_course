# Stage 3 — Deploy Checklist Template

Copy this template into your project root as `deploy-checklist.md` and update each section as you move toward launch.

## 1. Preflight
- [ ] `npm run lint` (or `pnpm`/`yarn`) passes.
- [ ] `npm run test` passes (list key suites run).
- [ ] Manual QA run on latest build (`npm run build && npm run preview`).
- [ ] Feature flags/env variables documented.

## 2. Environment Variables
| Variable | Value Source | Notes |
| --- | --- | --- |
| `VITE_MEALDB_BASE_URL` | `https://www.themealdb.com/api/json/v1/1` | Safe to expose. |
| `VITE_ANALYTICS_KEY` | Render Secret `analytics_key` | Optional instrumentation. |

## 3. Deployment Steps
1. Merge `release/*` branch to `main` (following Git Flow workflow).
2. Push `main` branch to remote (`git push origin main`).
3. Trigger Render/Vercel build (link URIs).
4. Monitor build logs for warnings/errors.
5. Run post-deploy smoke tests:
   - [ ] Load Home page, confirm announcements render.
   - [ ] Create + complete a task; verify persistence after refresh.
   - [ ] Toggle menu favorite; verify state sync and counts update.
   - [ ] Hard reload to confirm cached API responses handled gracefully.

## 4. Rollback Plan
- Note latest stable deployment URL/tag.
- Describe steps to revert (e.g., re-deploy previous commit, disable new feature flag).

## 5. Demo Prep
- Talk track outline (problem → solution → tech highlights → retro).
- Screens or gifs captured and stored in `/demo-assets`.
- Backup plan if TheMealDB is unavailable (mock JSON, local fallback).

---

**Related Task:** [Stage 3 Task Brief](../../tasks.md)

