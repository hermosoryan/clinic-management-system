# DevOps Practices — Hospital / Clinic Management System

## 1. Automation

### CI/CD Pipeline (GitHub Actions)
- Automatically runs on every push to `main`
- Pipeline: Build → Test → Deploy → Smoke Test
- Zero manual deployment needed
- Pipeline completes in under 30 seconds

### Automated Testing
- Unit tests run automatically on every PR
- Integration tests run before deployment
- Smoke test verifies live site after deployment

## 2. Collaboration

### Branch Strategy
- `main` — production-ready code only
- `dev` — integration branch for features
- `feature/<name>` — individual feature branches
- `bugfix/<name>` — bug fix branches
- `hotfix/<name>` — urgent production fixes

### Code Review Process
- All changes go through Pull Requests
- CODEOWNERS file ensures proper review
- No direct commits to main branch
- Clear commit messages for traceability

### Team Communication
- Daily standups facilitated by Scrum Master
- Sprint planning every 2 weeks
- Retrospectives after each sprint

## 3. Monitoring

### Current Monitoring
- GitHub Actions shows pipeline status
- GitHub Pages uptime monitoring
- Smoke test checks HTTP 200 after deployment
- Error logs tracked in metrics-report.md

### KPIs Monitored
- Defect Rate: 1 bug/sprint ✅
- Lead Time: 3 days ✅
- Deployment Frequency: 3x/week ✅
- Response Time: 620ms ⚠️
- System Availability: 99.5% ✅

## 4. Feedback Loop

### Sprint Retrospectives
- What went well?
- What needs improvement?
- Action items for next sprint

### User Feedback
- Bug reports tracked in defect-log.md
- Feature requests added to backlog
- QA testing after each sprint

## 5. Cloud/DevOps Improvement

### Monitoring Alert Added
We added a monitoring alert step to the CI/CD pipeline that:
- Checks system response time after deployment
- Alerts team if response time exceeds 500ms
- Logs all deployment results to GitHub Actions

### Updated Pipeline with Monitoring Alert
```yaml
- name: Monitoring Alert
  run: |
    RESPONSE_TIME=$(curl -o /dev/null -s -w "%{time_total}" 
    https://hermosoryan.github.io/clinic-management-system/)
    echo "Response time: ${RESPONSE_TIME}s"
    if (( $(echo "$RESPONSE_TIME > 0.5" | bc -l) )); then
      echo "WARNING: Response time exceeds 500ms target!"
    else
      echo "Response time is within target."
    fi
```

## 6. Emerging Trends Applied

| Trend | How We Applied It |
|-------|-----------------|
| DevOps | CI/CD pipeline with GitHub Actions |
| Cloud Hosting | GitHub Pages for zero-cost deployment |
| Agile | Scrum framework with sprints |
| Shift-Left Testing | Tests run before deployment |
| Infrastructure as Code | Pipeline defined in YAML file |
| GitOps | All changes tracked via Git |

