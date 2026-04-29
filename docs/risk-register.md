# Risk Register — Hospital / Clinic Management System

| ID | Risk | Likelihood (1-5) | Impact (1-5) | Risk Score | Mitigation Plan | Risk Owner |
|----|------|-----------------|--------------|------------|-----------------|------------|
| R-01 | Data breach or unauthorized access to patient records | 3 | 5 | 15 | Implement role-based access control and encrypt sensitive data | Emanuel Bajarla |
| R-02 | System downtime during peak clinic hours | 3 | 4 | 12 | Set up automated backups and a failover server | Emanuel Bajarla |
| R-03 | Incorrect patient data entry by staff | 4 | 4 | 16 | Add input validation and confirmation prompts on all forms | Trisha Aira Pabonita |
| R-04 | Appointment booking conflicts or double bookings | 3 | 3 | 9 | Implement real-time schedule locking during booking | Emanuel Bajarla |
| R-05 | Team member unavailability due to illness or emergency | 2 | 4 | 8 | Cross-train team members on each other's tasks | Sofia Belle Villarente |
| R-06 | Scope creep causing delays in sprint delivery | 4 | 3 | 12 | Strictly follow sprint backlog and review changes with Product Owner | Ryan Hermoso |
| R-07 | Poor UI/UX leading to low user adoption | 3 | 3 | 9 | Conduct user testing after each sprint and gather feedback | Trisha Aira Pabonita |
| R-08 | Integration failure between frontend and backend | 3 | 4 | 12 | Define clear API contracts and test integrations early | Mitch Dumdum |

| R-09 | SQL Injection attack on patient database | 3 | 5 | 15 | Use parameterized queries and ORM | Emanuel Bajarla |
| R-10 | Unauthorized access to patient records | 3 | 5 | 15 | Implement role-based access control | Emanuel Bajarla |
| R-11 | Cross-site scripting (XSS) attack on forms | 3 | 4 | 12 | Sanitize all user inputs on frontend | Trisha Aira Pabonita |