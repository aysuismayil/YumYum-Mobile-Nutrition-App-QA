# YumYum Mobile Nutrition App – QA

QA portfolio project with my manual testing work on **YumYum**, a publicly available iOS app that helps parents track the foods their baby eats.

> This is my independent QA portfolio project. I am not employed by, affiliated with, or representing YumYum. The repository does not include any internal company documents.

This is an active project. I add new artifacts as I complete them.

---

## What is in this repository

| Artifact | Link | What it contains |
|---|---|---|
| Product overview | [docs/product-overview.md](docs/product-overview.md) | Short overview of the app and the subscription rules I tested, in my own words |
| Test Plan | [docs/test-plan-subscription.md](docs/test-plan-subscription.md) | Test Plan for the Subscription feature (Free / Premium) |
| Test strategy and approach | [docs/test-strategy-and-approach.md](docs/test-strategy-and-approach.md) | How I test this app and why |
| Clarification questions | [docs/clarification-questions.md](docs/clarification-questions.md) | Open questions from my requirements review |
| Subscription test cases | [test-cases/subscription-test-cases.md](test-cases/subscription-test-cases.md) | SUB - 001 to SUB - 012 (SUB - 012 is Out of Scope) |
| Regression test cases | [test-cases/regression-test-cases.md](test-cases/regression-test-cases.md) | TC-REG-001 to TC-REG-004, written from confirmed bugs (not run yet) |
| Bug reports | [bug-reports/README.md](bug-reports/README.md) | BUG-001 to BUG-005, with the BUG ID ↔ GitHub Issue mapping |
| Exploratory testing notes | [exploratory-testing/exploratory-testing-notes.md](exploratory-testing/exploratory-testing-notes.md) | Notes from exploratory sessions |
| QA progress log | [docs/qa-progress-log.md](docs/qa-progress-log.md) | Dated log of QA work |
| Bug report template | [templates/bug-report-template.md](templates/bug-report-template.md) | The structure I use for every bug |

Bugs are also tracked as [GitHub Issues](https://github.com/aysuismayil/YumYum-Mobile-Nutrition-App-QA/issues) and on the GitHub Project board **Mobile Nutrition App - QA**
(Backlog → Ready for Testing → In Progress → Bug Reported → Ready for Retest → Done).

---

## How the documents connect

**Requirement → Test Case → Bug**

Subscription rules (free food-log limit + return to Free after Premium expires) → [SUB - 002](test-cases/subscription-test-cases.md#sub---002) → [BUG-001](bug-reports/BUG-001.md). **Partial:** what should happen to unused free food logs after Premium expires is not clearly defined (see gap G-1 in the [product overview](docs/product-overview.md#requirement-gap)).

BUG-002 to BUG-005 come from exploratory testing of the core app (food tracking, 7-Day Challenge, notifications, Baby Profile). They were not found while running the Subscription Test Plan. Each one has a regression test case.

---

## Current status

| Area | Status |
|---|---|
| Subscription Test Plan | Done (v1.0) |
| Subscription test cases | Written. Not executed yet. I am adding them to TestRail. |
| Exploratory testing | Done for the core flow. 4 bugs found. |
| Bug reports | 5 bugs reported. All are open. |
| Regression test cases | Written from the 4 exploratory bugs. Not executed yet. |
| Test Run / regression results | Not done yet |
| E2E, accessibility, performance testing | Not done yet |

Testing was done on a real iPhone 16 Pro. The exact app build and iOS version are in each bug report.

---

## Repository structure

```
README.md
docs/
  product-overview.md
  test-plan-subscription.md
  test-strategy-and-approach.md
  clarification-questions.md
  qa-progress-log.md
test-cases/
  subscription-test-cases.md
  regression-test-cases.md
bug-reports/
  README.md
  BUG-001.md … BUG-005.md
exploratory-testing/
  exploratory-testing-notes.md
templates/
  bug-report-template.md
```

---

**Aysu Ismayilzada** · QA Engineer
[GitHub](https://github.com/aysuismayil) · [Portfolio](https://aysuismayil.github.io)
