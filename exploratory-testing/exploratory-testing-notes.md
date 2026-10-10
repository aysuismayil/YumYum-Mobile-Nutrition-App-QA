# Exploratory Testing Notes

[← Back to README](../README.md)

Notes from exploratory sessions on the YumYum iOS app. New sessions are added by date.

## Session – August 31, 2026

**Focus:** product and requirements review, plus exploratory testing of the 7-Day Challenge and related notifications.

**What I did** (see the [QA progress log](../docs/qa-progress-log.md)):
- Continued product and requirements review
- Worked through [clarification questions](../docs/clarification-questions.md)
- Exploratory testing of the iOS app
- Tested Challenge behavior
- Investigated state after logout/login
- Reproduced a Challenge-related defect
- Recorded video evidence of the reproduction
- Documented the defect with the [bug report template](../templates/bug-report-template.md)
- Continued investigating push-notification behavior

**Finding:** 7-Day Challenge progress goes back to "Start 7 days challenge" after logging out and back in. Reported as [BUG-005](../bug-reports/BUG-005.md) ([Issue #1](https://github.com/aysuismayil/YumYum-Mobile-Nutrition-App-QA/issues/1)).

## Later sessions (dates not logged)

The other three core-app bugs came from more exploratory testing of the same flow: Tracker → Food Garden → 7-Day Challenge → notifications. I changed the order and timing of actions instead of only following the happy path.

- Logging a food for a **past date** instead of today, then checking which day the 7-Day Challenge marked complete → [BUG-002](../bug-reports/BUG-002.md) ([Issue #4](https://github.com/aysuismayil/YumYum-Mobile-Nutrition-App-QA/issues/4)).
- Updating the **Baby Profile** (name and date of birth), then checking the next push notification → [BUG-003](../bug-reports/BUG-003.md) ([Issue #2](https://github.com/aysuismayil/YumYum-Mobile-Nutrition-App-QA/issues/2)).
- Logging a food **before** a scheduled Challenge reminder, then checking whether the reminder was still sent → [BUG-004](../bug-reports/BUG-004.md) ([Issue #3](https://github.com/aysuismayil/YumYum-Mobile-Nutrition-App-QA/issues/3)).

[BUG-001](../bug-reports/BUG-001.md) came from Subscription testing, not from these sessions.
