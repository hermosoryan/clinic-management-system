# System Architecture — Hospital / Clinic Management System

## Architecture Overview
The system follows a client-server architecture deployed on GitHub Pages
with a CI/CD pipeline managed by GitHub Actions.

## ASCII Architecture Diagram

┌─────────────────────────────────────────────────────┐
│                    USERS                            │
│  Patient │ Doctor │ Receptionist │ Admin            │
└────────────────────┬────────────────────────────────┘
│ HTTP Request
▼
┌─────────────────────────────────────────────────────┐
│              FRONTEND LAYER                         │
│  HTML/CSS/JavaScript                                │
│  - Patient Registration Form                        │
│  - Appointment Booking Form                         │
│  - Doctor Schedule Viewer                           │
│  - Billing Module                                   │
│  Hosted on: GitHub Pages                            │
└────────────────────┬────────────────────────────────┘
│ API Calls
▼
┌─────────────────────────────────────────────────────┐
│              BACKEND LAYER                          │
│  Node.js / Express API                              │
│  - Authentication (Token-based)                     │
│  - Input Validation                                 │
│  - Business Logic                                   │
│  - Role-Based Access Control                        │
└────────────────────┬────────────────────────────────┘
│ Queries
▼
┌─────────────────────────────────────────────────────┐
│              DATABASE LAYER                         │
│  - Patient Records                                  │
│  - Appointment Data                                 │
│  - Billing Information                              │
│  - Doctor Profiles                                  │
└─────────────────────────────────────────────────────┘

CI/CD Pipeline Flow
Developer → Push to main → GitHub Actions
│
▼
Build → Test → Deploy → Smoke Test
│
▼
GitHub Pages (Live Site)

## Components

| Component | Technology | Purpose |
|-----------|-----------|---------|
| Frontend | HTML/CSS/JS | User interface |
| Backend | Node.js/Express | API and business logic |
| Database | MySQL/PostgreSQL | Data storage |
| CI/CD | GitHub Actions | Automated pipeline |
| Hosting | GitHub Pages | Static site hosting |
| Version Control | Git/GitHub | Code management |

## Data Flow
1. User opens browser and visits GitHub Pages URL
2. Frontend loads HTML/CSS/JavaScript files
3. User fills in a form (e.g., appointment booking)
4. Frontend sends API request to backend
5. Backend validates token and input data
6. Backend processes request and queries database
7. Database returns results to backend
8. Backend sends response to frontend
9. Frontend displays result to user

