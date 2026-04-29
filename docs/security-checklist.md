# Security Checklist — Hospital / Clinic Management System

## 1. Input Validation

### Form 1 — Patient Registration Form
- [x] Name field: rejects empty input
- [x] Age field: rejects non-numeric values
- [x] Email field: validates correct email format
- [x] Phone field: rejects letters and special characters

### Form 2 — Appointment Booking Form
- [x] Date field: rejects past dates
- [x] Time field: rejects empty input
- [x] Doctor selection: rejects empty selection
- [x] Patient ID: rejects non-numeric values

## 2. Basic Authentication / Authorization

### Token-Based Authentication
- [x] All API endpoints require a valid token
- [x] Token is stored securely in environment variables
- [x] Expired tokens are rejected
- [x] Unauthorized users cannot access patient records

### Example Token Validation
```javascript
function validateToken(token) {
  if (!token) {
    return { valid: false, message: 'No token provided' };
  }
  if (token !== process.env.DEPLOY_TOKEN) {
    return { valid: false, message: 'Invalid token' };
  }
  return { valid: true, message: 'Token is valid' };
}
```

## 3. Protected Sensitive Values
- [x] DEPLOY_TOKEN stored in GitHub Secrets
- [x] No hardcoded passwords in source code
- [x] No API keys exposed in public files
- [x] Environment variables used for all sensitive data

## 4. Dependency Audit

### Audit Command Used
```bash
npm audit
```

### Audit Results

### Audit Summary
| Package | Version | Vulnerability | Status |
|---------|---------|--------------|--------|
| No vulnerabilities found | - | - | ✅ Clean |

## 5. Logging & Least Privilege
- [x] Errors are logged without exposing sensitive data
- [x] Users can only access their own records
- [x] Admin functions restricted to admin role only
- [x] Doctor can only view their own patients

## 6. Security Risks Added to Risk Register

| ID | Risk | Likelihood | Impact | Score | Mitigation | Owner |
|----|------|-----------|--------|-------|------------|-------|
| R-09 | SQL Injection attack on patient database | 3 | 5 | 15 | Use parameterized queries and ORM | Emanuel Bajarla |
| R-10 | Unauthorized access to patient records | 3 | 5 | 15 | Implement role-based access control | Emanuel Bajarla |
| R-11 | Cross-site scripting (XSS) attack on forms | 3 | 4 | 12 | Sanitize all user inputs on frontend | Trisha Aira Pabonita |

