# CI/CD Pipeline Diagram — Hospital / Clinic Management System

## Pipeline Trigger
- Runs automatically on every push to `main` branch

## Pipeline Stages

## 1. TRIGGER
- Event: Push to main
- Tool: GitHub Actions

## 2. BUILD
- Checkout code
- Build project files

## 3. TEST
- Run unit tests
- Run integration tests
- If FAIL → Stop pipeline and notify team

## 4. DEPLOY
- Deploy to GitHub Pages
- Uses DEPLOY_TOKEN secret

## 5. SMOKE TEST
- Check homepage loads
- Verify HTTP status returns 200 OK
- If FAIL → Rollback to previous version

## Pipeline Table

| Stage | Action | Status |
|-------|--------|--------|
| Trigger | Push to main | ✅ Active |
| Build | Checkout + build | ✅ Active |
| Test | Run all tests | ✅ Active |
| Deploy | Push to GitHub Pages | ✅ Active |
| Smoke Test | Check 200 OK | ✅ Active |