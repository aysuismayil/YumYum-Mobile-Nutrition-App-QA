# Test Strategy and Approach – YumYum

[← Back to README](../README.md)

How I test this app and why. The [Test Plan](test-plan-subscription.md) covers the Subscription feature. This page covers my overall approach, including the core app flow.

---

## 1. Understand the business goal

The core loop of the app is simple: a parent logs the foods their baby eats. The Food Garden and the 7-Day Challenge make logging feel rewarding, so parents come back every day. Premium turns that habit into revenue.

This affects test priority. A bug that breaks the daily logging habit (for example [BUG-005](../bug-reports/BUG-005.md), where a paid user's Challenge resets after logging out) is a business problem, not only a UI problem.

## 2. Review requirements and ask questions

- For the **Subscription** feature, I wrote a [Test Plan](test-plan-subscription.md) and [test cases](../test-cases/subscription-test-cases.md) based on the subscription rules. While reviewing them, I found a gap (G-1 in the [product overview](product-overview.md#requirement-gap)). This gap is linked to [BUG-001](../bug-reports/BUG-001.md).
- For the **core app** (Tracker, Food Garden, 7-Day Challenge, notifications), I learned the expected behavior by using the app as a parent would. I wrote down open questions in [clarification-questions.md](clarification-questions.md).

## 3. Exploratory testing first for the core app

Where expected behavior was not written down, I started with exploratory testing. This builds an accurate picture of how the app works before writing formal test cases. Writing detailed test cases against guesses can document the wrong expected behavior.

## 4. Risk-based priorities

| Priority | Area | Why |
|---|---|---|
| P0 | Core logging flow: Tracker → Food Garden → 7-Day Challenge | This is the main reason the app exists. A break here affects every user. |
| P0 | Subscription purchase and expiration | Directly affects money and access to paid features ([BUG-001](../bug-reports/BUG-001.md)). |
| P1 | State after logout/login | Confirmed bug: Challenge state resets after logout/login ([BUG-005](../bug-reports/BUG-005.md)). |
| P1 | Notification content | Confirmed bug: a notification showed the previous baby's name and age after a profile update ([BUG-003](../bug-reports/BUG-003.md)). |
| P2 | Notification timing | Confirmed bug: a reminder was sent even though food was already logged ([BUG-004](../bug-reports/BUG-004.md)). |
| P2 | Date handling in the Challenge | Confirmed bug: logging food for a past date marked the wrong day complete ([BUG-002](../bug-reports/BUG-002.md)). |

The four confirmed core-app bugs are the base of the [regression test cases](../test-cases/regression-test-cases.md).

## 5. Where the bugs came from

None of the 5 bugs came from the simple happy path. They came from edge cases about **timing and order of actions**:

| Edge case | Bug |
|---|---|
| Using leftover free food logs after Premium expires | [BUG-001](../bug-reports/BUG-001.md) |
| Logging food for a past date, not today | [BUG-002](../bug-reports/BUG-002.md) |
| Updating the Baby Profile, then checking the next notification | [BUG-003](../bug-reports/BUG-003.md) |
| Logging food before a scheduled reminder | [BUG-004](../bug-reports/BUG-004.md) |
| Logging out and back in after joining the Challenge | [BUG-005](../bug-reports/BUG-005.md) |

So future edge-case testing on this app should focus on order of actions and state changes (dates, logout/login, app restart, plan changes), not only invalid input.

## 6. Test types: done and not done

| Test type | Status |
|---|---|
| Exploratory testing | Done for the core flow (see [notes](../exploratory-testing/exploratory-testing-notes.md)) |
| Functional test case design | Done for Subscription (SUB - 001 to SUB - 012) |
| Test execution / Test Run | Not done yet |
| Regression | Test cases written from confirmed bugs. Not executed yet. |
| End-to-end | Not done yet. The critical user flow is described in the [product overview](product-overview.md#critical-user-flow). |
| Compatibility | Not done. All testing was on one iPhone 16 Pro. |
| Accessibility | Not done yet |
| Performance | Not done |
| API | Not in scope. Testing is through the app UI only. |

## 7. What coverage means in this project

Every confirmed bug has a clear, repeatable scenario (see the [bug reports](../bug-reports/README.md) and the GitHub Issues). New test cases will cover those scenarios first, because this app's bugs so far are in edge cases and order of actions, not in the basic happy path.
