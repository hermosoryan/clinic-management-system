# Technical Debt — Hospital / Clinic Management System

## What is Technical Debt?
Technical debt refers to shortcuts or poor practices in code that need to be fixed later to improve quality, maintainability, and performance.

## Technical Debt Items

| ID | Debt Item | Description | Priority | Status |
|----|-----------|-------------|----------|--------|
| TD-01 | Hardcoded patient data in forms | Patient data is hardcoded in the frontend instead of being fetched from the API | High | To Fix |
| TD-02 | No input validation on appointment form | The appointment booking form does not validate empty fields or wrong date formats | High | To Fix |
| TD-03 | Duplicate code in billing module | The billing calculation logic is repeated in 3 different files instead of using a shared function | Medium | To Fix |
| TD-04 | No error handling on API calls | API calls do not have try/catch blocks, causing silent failures when the server is down | Medium | To Fix |
| TD-05 | Inconsistent naming conventions | Some variables use camelCase and others use snake_case in the same file | Low | To Fix |

## Selected Debt to Fix: TD-03 — Duplicate code in billing module

### Before Refactoring
The billing calculation was duplicated in 3 files:

```javascript
// In receptionist.js
function calculateTotal(services) {
  let total = 0;
  for (let i = 0; i < services.length; i++) {
    total = total + services[i].price;
  }
  return total;
}

// In billing.js (same code repeated)
function calculateTotal(services) {
  let total = 0;
  for (let i = 0; i < services.length; i++) {
    total = total + services[i].price;
  }
  return total;
}
```

### After Refactoring
Created a shared utility function used by all modules:

```javascript
// In utils/billing-utils.js (shared)
function calculateTotal(services) {
  return services.reduce((total, service) => total + service.price, 0);
}

// In receptionist.js
import { calculateTotal } from './utils/billing-utils.js';

// In billing.js
import { calculateTotal } from './utils/billing-utils.js';
```

### Improvement
- Removed code duplication across 3 files
- Cleaner and shorter function using reduce()
- Easier to maintain — fix once, applies everywhere