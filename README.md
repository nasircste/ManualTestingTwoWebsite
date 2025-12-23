# QA Test Documentation — Single Excel Workbook (2 Web Apps + 2 Mobile Apps)

This repository contains professional QA documentation for two web applications and their two corresponding mobile applications. All artifacts are consolidated into a single Excel workbook with multiple sheets, covering Test Planning, Test Case Authoring, Test Execution, Defect Management, and Test Reporting.

Date: 2025-12-03

---

## Overview

- One Excel file includes all QA artifacts as separate sheets.
- Applies to:
  - Web App EchoGpt
  - Web App AppTestingSevice
  - Mobile App EchoGpt
  - Mobile App AppTestingSevice

---



## Workbook Structure (Sheets)

1. Plan
   - Scope, objectives, assumptions, risks
   - Timeline, milestones, entry/exit criteria
   - Roles & responsibilities
2. Requirements Map
   - Requirement/Story ID → Feature → Product (Web/Mobile) → Priority
3. Test Cases
   - Columns: `Case ID`, `Product`, `Module`, `Title`, `Preconditions`, `Steps`, `Expected Result`, `Priority`, `Requirement ID`, `Owner`
   - ID convention: `WEB-A-TC-001`, `WEB-B-TC-001`, `MOB-A-TC-001`, `MOB-B-TC-001`
4. Regression Suite
   - Core, smoke, and critical paths per product and release
5. Execution Log
   - Columns: `Run ID`, `Build/Release`, `Case ID`, `Status (Pass/Fail/Blocked/NR)`, `Tester`, `Date`, `Notes`
   - Build mapping for traceability
6. Defect Log
   - Columns: `Defect ID`, `Title`, `Severity (Critical/High/Medium/Low)`, `Priority (P0/P1/P2)`, `Status`, `Linked Case ID`, `Environment`, `Assignee`, `Opened/Updated Dates`, `Repro Steps`, `Evidence (links)`
   - Workflow: New → Open → In Progress → Fixed → Ready for QA → Verified → Closed
---

## Test Strategy

- Functional testing of core features and edge cases
- Compatibility: browsers, devices, OS versions
- Usability & accessibility (WCAG as applicable)
- Security: basic auth/authorization checks, vulnerability scanning (as applicable)
- Performance: smoke/baseline checks where feasible

---



## Test Environments

- Web
  - Browsers: Chrome, Firefox, Edge (latest)
  - Environments: Production 
- Mobile
  - Android: target API levels; physical devices/emulators
  - iOS: target iOS versions; devices/simulators
- Data setup: test data/mocks/seed scripts referenced in the Plan sheet

---

## Test Case Authoring Standards

- Clear `Preconditions`, step-by-step `Steps`, and precise `Expected Result`
- Traceability: `Requirement ID ↔ Case ID ↔ Defect ID ↔ Execution`
- Coverage matrix maintained via `Requirements Map` and `Test Cases` sheets

---

## Test Execution

- Status categories: Pass, Fail, Blocked, Not Run
- Build/Release mapping per `Execution Log`
- Regression suite defined in `Regression Suite`
- Entry criteria: stable build, test data ready
- Exit criteria:
  - Zero open Critical/High defects
  - Acceptable thresholds for Medium/Low
  - Target pass rate achieved (define in Plan)

---

## Defect Management

- Severity: Critical, High, Medium, Low
- Priority: P0, P1, P2
- Lifecycle:
  - New → Open → In Progress → Fixed → Ready for QA → Verified → Closed
- Ensure repro steps and evidence links are captured

---

## Viewing the Excel File

- GitHub’s web preview for `.xlsx` can be limited
- Recommended: download and open with Microsoft Excel or LibreOffice
- Consider Git LFS for large files

---



## Risks & Constraints

- Device/browser availability
- Test data readiness
- Third-party dependencies and downtime

---


