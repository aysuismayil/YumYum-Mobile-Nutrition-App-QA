# Product Overview – YumYum

[← Back to README](../README.md)

A short overview of the app, written in my own words. It includes only what is needed to understand my testing. It is not a product specification.

---

## What the app does

YumYum is an iOS app (iPhone and iPad) that helps a parent track the foods their baby eats.

Features I worked with during testing:

- **Food Tracker** – the parent logs a food the baby ate (for example "Apricot") and chooses the log date.
- **Meals** – the parent can log a meal with one or more foods.
- **Food Garden** – a collection of foods. The first time a food is logged, it is added to the Food Garden (the app shows "New food discovered. Apricot joins the Food Garden.").
- **7-Day Challenge** – a daily streak. Each day is shown as completed or missed. The app sends a push notification if food is not logged by a set time.
- **History** – a list of logged foods by date.
- **Baby Profile** – the baby's name and date of birth.
- **Push notifications** – reminders linked to the 7-Day Challenge and the Baby Profile.
- **Free and Premium plans** – see below.

## Subscription (Free / Premium)

The rules below are the ones my Subscription test cases are based on.

- A **Free** user has limits on some features (for example, a limited number of food logs and AI recipes). A Free user can log up to 3 standalone foods.
- A Free user can tap **Upgrade** and buy **Premium**. Plans: weekly, monthly and annual.
- A 7-day free trial is available.
- A Premium user can switch plans (upgrade or downgrade).
- When Premium expires, the account goes back to the Free plan. Saved content stays.
- A user with an expired subscription can renew it.
- Prices are shown in the local currency of the App Store region.

## Requirement gap

**G-1 – Free food logs after Premium expires**

- When Premium expires, the account goes back to the Free plan.
- A Free user can log up to 3 standalone foods.
- It is **not defined** what should happen to free food logs that the user did not use before buying Premium.

This gap is linked to [SUB - 002](../test-cases/subscription-test-cases.md#sub---002) and [BUG-001](../bug-reports/BUG-001.md).

## Traceability

| Rule | Test Case | Bug | Support |
|---|---|---|---|
| Free food-log limit + return to Free after Premium expires (see G-1) | [SUB - 002](../test-cases/subscription-test-cases.md#sub---002) | [BUG-001](../bug-reports/BUG-001.md) | **Partial.** The expected behavior after expiration is not defined. |

No other Requirement → Test Case → Bug links are claimed.

## Platform

- iOS: iPhone and iPad.
- My testing so far was on one real iPhone 16 Pro. Device, iOS version and app build are listed in each bug report.
- Android and web were not part of my testing.

## Critical user flow

The flow most of my testing is centered on:

**open the app → log a food in the Tracker → the food appears in History (and in the Food Garden if it is new) → the 7-Day Challenge day is marked complete → push notifications match the Challenge state.**

BUG-002 to BUG-005 are all in this flow.
