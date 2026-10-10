# TEST CASES for "Subscription"

YumYum – iOS. Related document: [Subscription Test Plan](../docs/test-plan-subscription.md)

[← Back to README](../README.md)

> These test cases have not been executed yet. The **Actual Result** field is filled in during test execution, so it is empty here. I am adding these test cases to TestRail.

---

## Free User Enrollment

### SUB - 001

| Field | Value |
|---|---|
| **Priority** | P0 |
| **Title** | Free User who used all Free limits enrolls in any subscription |
| **Pre-conditions** | 1. User is signed in and has a baby profile.<br>2. User is a Free user. |
| **Test Data** | Free user account<br>Any available subscription plan |
| **Test Steps** | 1. Launch the app.<br>2. Use all Free limits for Product Log, AI Recipe, and Favorites.<br>3. Tap Upgrade.<br>4. Select any subscription plan.<br>5. Complete the subscription purchase.<br>6. Let the subscription expire.<br>7. Try to use a limited feature. |
| **Expected Result** | 1. Subscription is activated.<br>2. After expiration, "Upgrade to Premium" is displayed. |
| **Actual Result** | |

### SUB - 002

| Field | Value |
|---|---|
| **Priority** | P0 |
| **Title** | Free User With Partially Used Free Limits Enrolls in Subscription |
| **Pre-conditions** | 1. User is signed in and has a baby profile.<br>2. User is a Free user. |
| **Test Data** | Free user account<br>Any available subscription plan |
| **Test Steps** | 1. Launch the app.<br>2. Use part of the Free limits.<br>3. Tap Upgrade.<br>4. Select any subscription plan.<br>5. Complete the subscription purchase.<br>6. Let the subscription expire.<br>7. Try to use the remaining Free limits. |
| **Expected Result** | 1. Subscription is activated.<br>2. After expiration, remaining Free limits are available. |
| **Actual Result** | |
| **Related Bug** | [BUG-001](../bug-reports/BUG-001.md) – Unable to use remaining Free Food Logs after Premium expires |
| **Related gap** | [G-1](../docs/product-overview.md#requirement-gap) – behavior of unused free food logs after Premium expires is not defined |

### SUB - 003

| Field | Value |
|---|---|
| **Priority** | P1 |
| **Title** | Free User With Unused Free Limits Enrolls in Subscription |
| **Pre-conditions** | 1. User is signed in and has a baby profile.<br>2. User is a Free user.<br>3. User has not used any Free limits. |
| **Test Data** | Free user account<br>Any available subscription plan |
| **Test Steps** | 1. Launch the app.<br>2. Tap Upgrade.<br>3. Select any subscription plan.<br>4. Complete the subscription purchase.<br>5. Let the subscription expire.<br>6. Try to use Free features. |
| **Expected Result** | 1. Subscription is activated.<br>2. After expiration, all Free limits are available. |
| **Actual Result** | |

---

## New User Subscription

### SUB - 004

| Field | Value |
|---|---|
| **Priority** | P0 |
| **Title** | New User Enrolls in Monthly Subscription |
| **Pre-conditions** | 1. User is signed in and has a baby profile.<br>2. User has never had a subscription before. |
| **Test Data** | New user account<br>Plan: Monthly |
| **Test Steps** | 1. Launch the app.<br>2. Open Subscription.<br>3. Select Monthly plan.<br>4. Complete the subscription purchase.<br>5. Open Settings. |
| **Expected Result** | 1. Monthly subscription is activated.<br>2. Crown icon is purple.<br>3. Monthly plan is displayed in Settings. |
| **Actual Result** | |

### SUB - 005

| Field | Value |
|---|---|
| **Priority** | P0 |
| **Title** | New User Enrolls in Annual Subscription |
| **Pre-conditions** | 1. User is signed in and has a baby profile.<br>2. User has never had a subscription before. |
| **Test Data** | New user account<br>Plan: Annual |
| **Test Steps** | 1. Launch the app.<br>2. Tap Upgrade.<br>3. Select Annual plan.<br>4. Complete the subscription purchase.<br>5. Open Settings. |
| **Expected Result** | 1. Annual subscription is activated.<br>2. Crown icon is purple.<br>3. Annual plan is displayed in Settings. |
| **Actual Result** | |

---

## Premium User Subscription

### SUB - 006

| Field | Value |
|---|---|
| **Priority** | P0 |
| **Title** | User Is Able to Upgrade Subscription Plan From Weekly to Monthly |
| **Pre-conditions** | 1. User is signed in and has a baby profile.<br>2. User has an active Weekly subscription. |
| **Test Data** | Premium user account<br>Current plan: Weekly<br>New plan: Monthly |
| **Test Steps** | 1. Launch the app.<br>2. Open Subscription.<br>3. Upgrade from Weekly to Monthly.<br>4. Open Settings. |
| **Expected Result** | 1. Subscription is upgraded from Weekly to Monthly.<br>2. Crown icon is purple.<br>3. Monthly plan is displayed in Settings. |
| **Actual Result** | |

### SUB - 007

| Field | Value |
|---|---|
| **Priority** | P0 |
| **Title** | User Is Able to Downgrade Subscription Plan From Annual to Weekly |
| **Pre-conditions** | 1. User is signed in and has a baby profile.<br>2. User has an active Annual subscription. |
| **Test Data** | Premium user account<br>Current plan: Annual<br>New plan: Weekly |
| **Test Steps** | 1. Launch the app.<br>2. Open Subscription.<br>3. Downgrade from Annual to Weekly.<br>4. Open Settings. |
| **Expected Result** | 1. Subscription is downgraded from Annual to Weekly.<br>2. Crown icon is purple.<br>3. Weekly plan is displayed in Settings. |
| **Actual Result** | |

### SUB - 008

| Field | Value |
|---|---|
| **Priority** | P0 |
| **Title** | User Is Not Able to Enroll in the Same Subscription Plan Twice |
| **Pre-conditions** | 1. User is signed in and has a baby profile.<br>2. User has an active subscription. |
| **Test Data** | Premium user account<br>Active subscription plan |
| **Test Steps** | 1. Launch the app.<br>2. Open Subscription.<br>3. Select the same active plan.<br>4. Try to enroll again. |
| **Expected Result** | 1. User cannot enroll in the same plan twice.<br>2. "You already enrolled" message is displayed. |
| **Actual Result** | |

---

## Free Trial & Renewal

### SUB - 009

| Field | Value |
|---|---|
| **Priority** | P0 |
| **Title** | User Enrolled in 7-Day Free Trial Is Able to Enroll in Subscription |
| **Pre-conditions** | 1. User is signed in and has a baby profile.<br>2. User is enrolled in the 7-day Free Trial. |
| **Test Data** | User account enrolled in 7-Day Free Trial<br>Any available subscription plan |
| **Test Steps** | 1. Launch the app with an active 7-Day Free Trial.<br>2. Tap the Crown icon or open Settings → Subscription.<br>3. Tap Upgrade.<br>4. Select any available subscription plan.<br>5. Complete the subscription purchase.<br>6. Open Settings → Subscription. |
| **Expected Result** | 1. User is enrolled in the selected subscription.<br>2. Crown icon is purple.<br>3. Selected subscription plan is displayed in Settings. |
| **Actual Result** | |

### SUB - 010

| Field | Value |
|---|---|
| **Priority** | P0 |
| **Title** | User Whose Subscription Expired Is Able to Renew Subscription |
| **Pre-conditions** | 1. User is signed in and has a baby profile.<br>2. User's subscription has expired. |
| **Test Data** | User account with expired subscription<br>Any available subscription plan |
| **Test Steps** | 1. Launch the app.<br>2. Tap the Crown icon.<br>3. Select any available subscription plan.<br>4. Complete the subscription purchase.<br>5. Open Settings → Subscription. |
| **Expected Result** | 1. Subscription is renewed.<br>2. Crown icon is purple.<br>3. Selected subscription plan is displayed in Settings. |
| **Actual Result** | |

### SUB - 011

| Field | Value |
|---|---|
| **Priority** | P1 |
| **Title** | Verify Subscription Localization |
| **Pre-conditions** | 1. User is signed in.<br>2. Subscription is available. |
| **Test Data** | Region: USA / Europe |
| **Test Steps** | 1. Launch the app.<br>2. Open Subscription.<br>3. Set the region to USA.<br>4. Check the subscription currency.<br>5. Set the region to Europe.<br>6. Check the subscription currency. |
| **Expected Result** | 1. USA displays USD.<br>2. Europe displays EUR. |
| **Actual Result** | |

---

## Out of Scope

> Listed for reference only. Subscription Cancellation is Out of Scope in the [Subscription Test Plan](../docs/test-plan-subscription.md). This test case is not part of in-scope Subscription testing.

### SUB - 012

| Field | Value |
|---|---|
| **Priority** | Not set |
| **Title** | User Is Able to Cancel Subscription |
| **Pre-conditions** | 1. User is signed in and has an active subscription.<br>2. Subscription can be canceled at any time. |
| **Test Data** | User account with active subscription |
| **Test Steps** | 1. Launch the app.<br>2. Open Subscription.<br>3. Cancel the active subscription. |
| **Expected Result** | 1. Subscription is cancelled according to Terms and Conditions. |
| **Actual Result** | |
