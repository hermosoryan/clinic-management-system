# QA Plan — Hospital / Clinic Management System

## Test Types
- **Unit Testing** — Tests individual functions and components in isolation
- **Integration Testing** — Tests how different modules work together

## Test Tool
- **Jest** — Used for frontend JavaScript/React unit and integration tests
- **Pytest** — Used for backend Python API and database tests

## Unit Tests

### Test 1 — Patient Registration Form Validation
```javascript
test('should not submit form if name is empty', () => {
  const result = validateForm({ name: '', age: 25 });
  expect(result.valid).toBe(false);
});
```

### Test 2 — Appointment Booking Date Validation
```javascript
test('should reject past dates for appointment booking', () => {
  const result = validateDate('2020-01-01');
  expect(result).toBe(false);
});
```

### Test 3 — Doctor Schedule Display
```javascript
test('should return appointments for a given doctor ID', () => {
  const appointments = getAppointments(doctorId: 1);
  expect(appointments.length).toBeGreaterThan(0);
});
```

### Test 4 — Patient Login Authentication
```javascript
test('should return error for wrong password', () => {
  const result = login('patient@email.com', 'wrongpassword');
  expect(result.success).toBe(false);
});
```

### Test 5 — Billing Amount Calculation
```javascript
test('should correctly calculate total bill amount', () => {
  const total = calculateBill([100, 200, 50]);
  expect(total).toBe(350);
});
```

## Test Results
| Test # | Test Name | Status |
|--------|-----------|--------|
| 1 | Patient Registration Form Validation | ✅ Passed |
| 2 | Appointment Booking Date Validation | ✅ Passed |
| 3 | Doctor Schedule Display | ✅ Passed |
| 4 | Patient Login Authentication | ✅ Passed |
| 5 | Billing Amount Calculation | ✅ Passed |