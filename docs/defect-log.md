# Defect Log — Hospital / Clinic Management System

## Bug Report

| Field | Details |
|-------|---------|
| **Bug ID** | BUG-001 |
| **Title** | Appointment booking allows past dates |
| **Reported By** | Mitch Dumdum |
| **Date Reported** | April 24, 2026 |
| **Severity** | High |
| **Status** | Closed ✅ |

## Description
When a patient tries to book an appointment, the date picker allowed selection of past dates. This caused invalid appointments to be saved in the system.

## Steps to Reproduce
1. Log in as a patient
2. Go to "Book Appointment"
3. Select a date from last month
4. Click "Confirm Booking"
5. System accepted the booking — **this is the bug**

## Fix Applied
Added a date validation check in the frontend that disables all past dates in the date picker. Added backend validation to reject any appointment date earlier than today's date.

## Fix Verified By
Mitch Dumdum — April 24, 2026

## Final Status: Closed ✅