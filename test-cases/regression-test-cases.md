# Regression Test Cases

[← Back to README](../README.md)

**Status: written, not executed yet.** These four test cases come from the four confirmed core-app bugs (BUG-002 to BUG-005). I will run them after the bugs are fixed and add the real results here.

Format: ID, Priority, Title, Linked bug, Preconditions, Test Data, Test Steps, Expected Result, Status.

---

## TC-REG-001 – 7-Day Challenge progress stays after logout/login

- **Priority:** P1
- **Linked bug:** [BUG-005](../bug-reports/BUG-005.md) ([Issue #1](https://github.com/aysuismayil/YumYum-Mobile-Nutrition-App-QA/issues/1))
- **Preconditions:** User is logged in with an active 7-Day Challenge in progress (at least one day completed).
- **Test Data:** Existing account with partial Challenge progress.
- **Test Steps:**
  1. Note the current 7-Day Challenge status (days completed).
  2. Log out of the app.
  3. Log back in with the same account.
  4. Go to the 7-Day Challenge screen.
- **Expected Result:** The Challenge shows the same progress as before logout. No days are lost.
- **Status:** Not executed yet. Linked bug is open.

## TC-REG-002 – Push notification shows the current Baby Profile after an update

- **Priority:** P1
- **Linked bug:** [BUG-003](../bug-reports/BUG-003.md) ([Issue #2](https://github.com/aysuismayil/YumYum-Mobile-Nutrition-App-QA/issues/2))
- **Preconditions:** User has a Baby Profile with a name and date of birth, and push notifications are enabled.
- **Test Data:** A Baby Profile update (new name and/or date of birth).
- **Test Steps:**
  1. Update the Baby Profile's name and/or date of birth.
  2. Save the change.
  3. Wait for a push notification that shows the baby's name/age.
- **Expected Result:** The notification shows the updated name/age.
- **Status:** Not executed yet. Linked bug is open.

## TC-REG-003 – Challenge reminder is not sent when food is already logged

- **Priority:** P2
- **Linked bug:** [BUG-004](../bug-reports/BUG-004.md) ([Issue #3](https://github.com/aysuismayil/YumYum-Mobile-Nutrition-App-QA/issues/3))
- **Preconditions:** User is enrolled in the 7-Day Challenge. A Challenge reminder notification is scheduled (9 AM).
- **Test Data:** A food entry logged before the reminder time.
- **Test Steps:**
  1. Log a food for the current day before the reminder time.
  2. Wait until the reminder time passes.
  3. Check whether the reminder notification is received.
- **Expected Result:** The reminder is not sent, because food is already logged for the day.
- **Status:** Not executed yet. Linked bug is open.

## TC-REG-004 – 7-Day Challenge marks the correct day when food is logged for a past date

- **Priority:** P2
- **Linked bug:** [BUG-002](../bug-reports/BUG-002.md) ([Issue #4](https://github.com/aysuismayil/YumYum-Mobile-Nutrition-App-QA/issues/4))
- **Preconditions:** User has an active 7-Day Challenge. Today is not completed yet.
- **Test Data:** A food entry (for example "Apricot") logged for a past date.
- **Test Steps:**
  1. Open the Tracker and log a food.
  2. Set the log date to a past date (not today).
  3. Save the entry.
  4. Open the 7-Day Challenge screen.
- **Expected Result:** The food counts for the selected past date. Today is not marked as completed because of a past-dated entry.
- **Status:** Not executed yet. Linked bug is open.
