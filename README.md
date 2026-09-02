# Manual QA Testing Project — CuraHealthcare Demo Application

## Overview
This project demonstrates manual testing of the CuraHealthcare Service demo application, a healthcare appointment booking system. The goal was to design and execute test cases covering the Login and Make Appointment workflows, and to identify, document, and report real defects using standard QA practices.

## Scope
- Login functionality (username/password validation)
- Appointment booking functionality (Facility selection, Visit Date, Comment, Hospital Readmission, Healthcare Program)

## Approach
Test cases were designed using a mix of testing techniques:
- **Positive testing** — valid inputs, expected successful flows
- **Negative testing** — invalid inputs, empty fields, incorrect credentials
- **Boundary value testing** — unusually long input (50+ character username)
- **Special character testing** — non-standard characters in input fields

Each test case was manually executed against the live application, with actual results recorded and compared against expected results to determine Pass/Fail status.

## Test Summary
- **Total test cases designed and executed:** 12
- **Passed:** 11
- **Failed:** 1
- **Defects found:** 1

## Defect Found
**BUG_01 — System allows appointment booking with a past date**
The application does not validate the Visit Date field against the current date, allowing users to successfully book appointments in the past. This is a logical/business-rule validation gap in a healthcare scheduling context.
- **Severity:** Medium
- **Priority:** High

Full details in [`Bug_Report.xlsx`](./Bug_Report.xlsx), with supporting screenshot in the `Screenshots` folder.

## Files in this repository
- `test_cases_login_appointment.xlsx` — full set of 12 test cases with steps, expected results, actual results, and pass/fail status
- `bug_report_BUG_01.md` — formal bug report for the defect found
- `Screenshots/` — supporting screenshot evidence

## Tools Used
- Google Sheets (test case design and execution logging)
- GitHub (project documentation and version control)
- CuraHealthcare demo application (application under test)

## What I Learned
This project helped me apply core manual QA concepts in practice — writing structured test cases, distinguishing positive/negative/boundary testing scenarios, executing tests methodically, and documenting a defect with proper severity and priority classification.

---
**Author:** Spoorthi Pai
