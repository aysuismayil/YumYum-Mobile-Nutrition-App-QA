# TEST PLAN

**Feature name:** "SUBSCRIPTION"
**Product:** YumYum (native iOS app: iPhone and iPad)
**Date:** September 2026

[← Back to README](../README.md)

---

## TABLE OF CONTENTS

- [Objective](#objective)
- [Product Overview](#product-overview)
- [Scope of Testing](#scope-of-testing)
- [Testing Strategy](#testing-strategy)
- [Test Documentation & Reporting](#test-documentation--reporting)
- [Test Deliverables](#test-deliverables)
- [Entry Criteria](#entry-criteria)
- [Suspension Criteria](#suspension-criteria)
- [Resumption Criteria](#resumption-criteria)
- [Exit Criteria (Definition of DONE)](#exit-criteria-definition-of-done)
- [Resources & Responsibilities](#resources--responsibilities)
- [Risks & Mitigations](#risks--mitigations)

---

## Revision History

| Version | Author | Date |
|---|---|---|
| 1.0 | Aysu Ismayilzada | 09/13/2026 |

---

## OBJECTIVE

This document describes the plan for testing the "Subscription" feature of the YumYum iOS app on iPhone and iPad. It defines the scope of testing, test strategy, test documentation, entry/exit criteria, risks and deliverables. The goal is to make sure users can buy, switch, renew and lose Premium access without problems.

## PRODUCT OVERVIEW

"Subscription" lets YumYum users buy a Premium plan and get access to Premium features. Users can choose a weekly, monthly or annual plan. Free users have limits on some features. See the [product overview](product-overview.md#subscription-free--premium) for the rules I tested.

## SCOPE OF TESTING

### Features To Be Tested (In Scope)

- **Free User**
  - Free user functionality and limits
  - Upgrade to Premium after reaching Free limits
- **Premium Subscription Plans**
  - Weekly Plan
  - Monthly Plan
  - Annual Plan
- **Subscription Plan Switching**
  - Subscription Plan Upgrade
  - Subscription Plan Downgrade
- **Duplicate Subscription Enrollment**
- **Free Trial and Renewal**
- **Localization** (currency by region)

### Features Not To Be Tested (Out of Scope)

- Sign Up / Sign In
- User Profile
- Food Garden
- 7-Day First Foods Challenge
- First 100 Foods
- Subscription Cancellation
- Subscription Refund
- Desktop Application
- Network connectivity

## TESTING STRATEGY

### Applications

**MOBILE:**
- iPhone
- iPad

### Test Levels

- System Testing

### Planned Test Types

- Smoke
- Functional
- Exploratory
- UI / Usability
- Regression
- Localization

### Compatibility

- iPhone and iPad
- Minimum iOS version: 17.0

### Tools

- Real iOS device (iPhone 16 Pro)
- GitHub Issues and GitHub Project board – bug tracking
- TestRail – test case management (test cases are being added)

## TEST DOCUMENTATION & REPORTING

- [Test Cases](../test-cases/subscription-test-cases.md)
- Test Run results (not done yet)
- [Traceability](product-overview.md#traceability)
- [Bug reports](../bug-reports/README.md)

When testing is finished, I will prepare a Readiness Summary Report based on the test results.

## TEST DELIVERABLES

| Deliverable | Status |
|---|---|
| Test Plan | Done |
| Test cases | Written, being added to TestRail |
| Test Run results | Not done yet |
| Bug reports | In progress (see [bug reports](../bug-reports/README.md)) |
| Regression results | Not done yet |
| Readiness Summary Report | Not done yet |

## ENTRY CRITERIA

- The build is in a testable condition (smoke test passed)
- Test cases are written and reviewed
- Test accounts and test data are available

## SUSPENSION CRITERIA

- The smoke test for the build fails (for example, a crash)
- A major function does not work

## RESUMPTION CRITERIA

- The suspension problem is resolved

## EXIT CRITERIA (Definition of DONE)

- All test cases are executed (test run rate is 100%)
- The PASS rate of test cases is no less than 80%
- No blockers or high-priority (P1) defects are open
- No more than 10% of low-severity issues are open (P2, P3)
- Workarounds for open low-severity issues are documented in the Readiness Summary Report
- The main subscription functions work according to the rules in the product overview
- The app is stable on the supported iOS version

## RESOURCES & RESPONSIBILITIES

| Name | Role | Responsibilities |
|---|---|---|
| Aysu | QA Engineer | Test planning, test case design, test execution, bug reporting, test documentation |

## RISKS & MITIGATIONS

| Risks | Mitigation |
|---|---|
| Requirements change often | Update test cases and review scope regularly |
| Limited time | Set test priority and test the critical path first |
| Known issues | Keep a list of known problems with workarounds |
| Network testing is out of scope | Note it as a known gap. Focus on UI, functionality and usability. |
