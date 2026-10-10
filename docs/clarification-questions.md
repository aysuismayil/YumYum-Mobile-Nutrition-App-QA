# Clarification Questions

[← Back to README](../README.md)

Open questions from my review of the app's behavior and the subscription rules. Several of them point to an unclear area where a bug was later confirmed.

## 7-Day Challenge

1. What should happen to 7-Day Challenge progress when a user logs out and logs back in? Should it stay? The actual behavior (progress resets) is reported as [BUG-005](../bug-reports/BUG-005.md) (Issue #1).
2. When food is logged for a past date instead of today, which day should the 7-Day Challenge mark as complete: the log date, or the day the entry was created? The app marks the wrong day: [BUG-002](../bug-reports/BUG-002.md) (Issue #4).

## Notifications

3. If the Baby Profile is updated (name, date of birth), how fast should the change show up in scheduled push notifications? The app showed the previous baby's name and age: [BUG-003](../bug-reports/BUG-003.md) (Issue #2).
4. If food is already logged before a scheduled reminder, should the reminder still be sent? The app sent it anyway: [BUG-004](../bug-reports/BUG-004.md) (Issue #3).

## Subscription

5. What should happen to unused free food logs after Premium expires? See gap G-1 in the [product overview](product-overview.md#requirement-gap) and [BUG-001](../bug-reports/BUG-001.md) (Issue #5).

## Platform

6. Is Android support planned? My testing covers iOS only.
