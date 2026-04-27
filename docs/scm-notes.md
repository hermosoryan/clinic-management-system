# SCM Notes — Merge Conflict Documentation

## What Happened
During Sprint 1 development, a merge conflict occurred in `README.md` when merging `conflict-branch` into `main`.

## Why It Happened
Two developers edited the same line in `README.md` at the same time:
- `main` branch had: `This is a change from main branch`
- `conflict-branch` had: `This is a change from conflict-branch`

## How We Resolved It
1. Ran `git merge conflict-branch` on main branch
2. Git detected: `CONFLICT (content): Merge conflict in README.md`
3. Opened `README.md` in VS Code
4. Saw the conflict markers:
5. Manually kept both lines and removed conflict markers
6. Ran `git add .`
7. Ran `git commit -m "Resolve merge conflict in README"`
8. Ran `git push origin main`

## Lesson Learned
Always pull the latest changes before starting new work to minimize conflicts.