# Demo Script — Hospital / Clinic Management System
## 5-7 Minute Presentation Guide

---

## 🎤 INTRODUCTION (30 seconds)

"Good day! I am Ryan Hermoso, Product Owner of Team 1.
Today I will demo our Hospital and Clinic Management System
built over 14 weeks using Agile, DevOps, and Software
Engineering best practices.
Let me walk you through our journey from problem to solution."

---

## 1. PROBLEM (1 minute)

"The problem we solved:"

- Clinics in the Philippines still use manual processes
- Appointment scheduling takes 30 minutes per day
- Patient records are stored in paper files
- Billing errors happen frequently due to manual calculations
- Doctors cannot quickly access patient history

"This leads to:"
- Wasted time for patients and staff
- Medical errors due to missing information
- Lost revenue due to billing mistakes
- Poor patient experience

---

## 2. SOLUTION (1 minute)

"Our solution is a web-based Hospital/Clinic Management System."

Show GitHub repository:
- docs/backlog.md — 10 user stories
- docs/sprint-1-plan.md — Sprint planning
- docs/team-roles.md — Team structure

"Our system provides:"
- Online patient registration
- Appointment booking with validation
- Doctor schedule management
- Digital billing and records
- Role-based access for all staff

"Our team:"
- Ryan Hermoso — Product Owner
- Sofia Belle Villarente — Scrum Master
- Emanuel Bajarla — Backend Developer
- Trisha Aira Pabonita — Frontend Developer
- Mitch Dumdum — QA Engineer

---

## 3. PIPELINE (1.5 minutes)

"We built a full CI/CD pipeline using GitHub Actions."

Show GitHub Actions page:
- github.com/hermosoryan/clinic-management-system/actions

"Every time we push code to main, the pipeline runs:"

Step 1 — BUILD
- Code is checked out
- Project is built automatically

Step 2 — TEST
- 5 unit tests run automatically
- All tests must pass before deployment

Step 3 — DEPLOY
- Code is deployed to GitHub Pages
- Uses DEPLOY_TOKEN secret for security

Step 4 — SMOKE TEST
- System checks if homepage returns 200 OK
- If it fails, team is alerted immediately

Show docs/cicd-diagram.md for the visual diagram.

"Result: Zero manual deployments needed!"

---

## 4. DEPLOYMENT (1 minute)

"Our system is live and accessible to anyone."

Show live site:
- https://hermosoryan.github.io/clinic-management-system

"Deployment details:"
- Platform: GitHub Pages (FREE)
- Auto-deploys on every push to main
- Deployment time: under 30 seconds
- Uptime: 99.5%

Show docs/deployment-plan.md:
- Blue-Green deployment strategy
- Clear rollback steps if something goes wrong

Show GitHub tags:
- github.com/hermosoryan/clinic-management-system/tags
- v0.5, v0.5-scm, v0.8-maintenance, v1.0

"We are now at version v1.0 — production ready!"

---

## 5. METRICS (1 minute)

"Let me show you our project performance."

Show docs/kpis.md and docs/metrics-report.md:

| KPI | Target | Actual | Status |
|-----|--------|--------|--------|
| Defect Rate | < 3 bugs | 1 bug | ✅ |
| Lead Time | < 5 days | 3 days | ✅ |
| Deployment Frequency | 2x/week | 3x/week | ✅ |
| Response Time | < 500ms | 620ms | ⚠️ |
| Availability | > 99% | 99.5% | ✅ |

Show docs/cost-benefit.md:
- Development Cost: $18,130
- Monthly Ops Cost: $135
- 3-Year ROI: 52.75%

"The system pays for itself in under 2 years!"

---

## 6. LESSONS LEARNED (1 minute)

"Here are the most important things our team learned:"

Technical Lessons:
- Always use feature branches — never commit directly to main
- CI/CD saves hours of manual work every week
- Input validation must be done on both frontend and backend
- Secrets must never be hardcoded — always use environment variables
- Tags help track versions and make rollbacks easy

Team Lessons:
- Clear commit messages help the whole team understand changes
- Pull Requests improve code quality through review
- Daily standups keep everyone aligned
- Breaking tasks into small user stories makes estimation easier

What we would do differently:
- Set up a real database from the start
- Add automated performance monitoring earlier
- Write more unit tests from Sprint 1

---

## 🎤 CLOSING (30 seconds)

"In summary, Team 1 successfully built and deployed a
Hospital/Clinic Management System that:

✅ Follows Agile/Scrum methodology
✅ Uses Git branching and Pull Requests
✅ Has a full CI/CD pipeline
✅ Is live and deployed on GitHub Pages
✅ Has a positive ROI of 52.75%
✅ Follows security best practices

Thank you for listening!
I am happy to answer any questions."

---

## 📋 Demo Checklist
- [ ] Open GitHub repository
- [ ] Show docs folder with all files
- [ ] Show GitHub Actions pipeline running
- [ ] Show live website
- [ ] Show GitHub tags (v1.0)
- [ ] Show KPIs and metrics
- [ ] Show cost-benefit ROI
- [ ] Ready to answer questions