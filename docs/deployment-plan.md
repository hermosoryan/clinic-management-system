# Deployment Plan — Hospital / Clinic Management System

## Target Environment
- **Platform:** GitHub Pages (Frontend)
- **Environment:** Development
- **URL:** https://hermosoryan.github.io/clinic-management-system

## Rollout Strategy
We will use a **Blue-Green Deployment** strategy:
1. Deploy new version to staging environment first
2. Run all tests on staging
3. Switch traffic from old version (blue) to new version (green)
4. Monitor for 24 hours before full release

## Deployment Steps
1. Merge all approved PRs into `main` branch
2. Run all unit and integration tests
3. Tag the release version (e.g., v1.0)
4. Push to GitHub Pages using `gh-pages` branch
5. Verify the deployed URL is working
6. Notify team via Slack/email

## Rollback Steps
If something goes wrong after deployment:
1. Immediately revert to previous tag:
```bash
git checkout v0.5
git push origin main --force
```
2. Notify the team of the rollback
3. Investigate and fix the issue on a hotfix branch:
```bash
git checkout -b hotfix/fix-issue
```
4. Re-deploy after fix is verified
5. Document what went wrong in `docs/scm-notes.md`