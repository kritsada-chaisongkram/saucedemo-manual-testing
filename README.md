# SauceDemo Manual Testing Portfolio

## Project Overview

I created this project to practice manual software testing using [SauceDemo](https://www.saucedemo.com/), a demo shopping website from Sauce Labs.

In this project, I wrote test cases, ran tests, checked results, reported bugs, and practiced end-to-end and regression testing.

- **Application Under Test:** SauceDemo
- **Testing Type:** Manual Testing
- **Test Environment:** Google Chrome, Windows 11
- **Test Management:** Excel
- **Bug Reports:** Jira-style reports with screenshots
- **Requirements:** [Portfolio-Derived Functional Requirements](requirements.md)

> **About the requirements:** I wrote the requirements based on the website's behavior and the test scenarios in this project. These are not official requirements from Sauce Labs.

## Quick Portfolio Review

Here are a few files you can review directly on GitHub before opening the Excel files:

1. [Sample test cases](test-cases/representative-test-cases.md) — two examples showing expected results, actual results, and screenshots.
2. [Requirements and traceability](requirements.md) — the requirements I used and their related test cases.
3. [Bug report: SCRUM-17](bug-reports/SCRUM-17/bug-report.md) — reproduction steps, price comparisons, and screenshots.
4. [Test summary report](test-results/test-summary-report.md) — test results, risks, limitations, and conclusion.

All Excel test cases, screenshots, and other files are linked below.

## Test Scope & Execution Summary

| Feature | Total Test Cases | Passed | Failed | Needs Clarification |
| :-- | --: | --: | --: | --: |
| Login | 8 | 8 | 0 | 0 |
| Product Listing | 5 | 5 | 0 | 0 |
| Product Details | 4 | 4 | 0 | 0 |
| Shopping Cart | 7 | 7 | 0 | 0 |
| Checkout & Order Flow | 8 | 7 | 0 | 1 |
| End-to-End Purchase | 1 | 1 | 0 | 0 |
| **Total** | **33** | **32** | **0** | **1** |

I executed 33 unique test cases, including one end-to-end test and one exploratory checkout test.

**Needs Clarification:** In `TC-CHECKOUT-006`, I entered special characters in the Postal Code field. The website accepted them, but I did not have an official rule for the allowed postal code format. I marked the case **Needs Clarification**, not PASS or FAIL.

## Testing Approach

I used these testing approaches:

- **Requirement Analysis:** Wrote practice requirements and acceptance criteria to guide the tests.
- **Functional Testing:** Checked shopping features against expected results.
- **Positive Testing:** Tested actions with valid inputs.
- **Negative Testing:** Tested invalid inputs, missing fields, and blocked access.
- **Input Validation Testing:** Checked required fields and how the website handled different inputs.
- **Access Control Testing:** Checked if users could open protected pages without logging in.
- **End-to-End Testing:** Tested the purchase flow from login to order confirmation.
- **Regression Testing:** Ran selected test cases again for a simulated change.
- **Exploratory Testing:** Checked unusual behavior and recorded issues I could reproduce.

The Excel test case files include actual results, test status, and evidence. Each test case also has a `Requirement ID` linked to [requirements.md](requirements.md).

The **Evidence** column in Excel links to screenshots on GitHub where available. Screenshots are grouped by Test Case ID. One screenshot may support more than one result.

## End-to-End Testing

I ran one end-to-end test to check the full purchase flow.

**TC-E2E-001 — End-to-End Purchase Flow with Two Products**

The test includes:

1. Login with a valid user account.
2. Select and add two products to the cart.
3. Verify cart contents.
4. Enter checkout information.
5. Verify order summary and price calculation.
6. Complete the order and verify confirmation.

**Execution Result:** 1 Passed, 0 Failed

- [E2E Test Cases & Execution Results](test-cases/e2e-test-cases.xlsx)
- [E2E Screenshot Evidence](test-evidence/e2e/)

## Regression Testing

I practiced regression testing using a **simulated developer fix** for the checkout total calculation. No real code was changed.

I ran three existing test cases again to check the cart and checkout.

| Test Case ID | Scenario | Status |
| :-- | :-- | :-- |
| TC-CART-005 | Shopping Cart Displays Added Products | PASS |
| TC-CHECKOUT-005 | Order Summary and Price Calculation Accuracy | PASS |
| TC-CHECKOUT-001 | Complete Successful Checkout Flow | PASS |

**Execution Result:** 3 Passed, 0 Failed

These were existing test cases run again, so they are not added to the 33 unique test cases.

**Limitation:** I did not test a real code fix or deployment.

- [Regression Testing Summary](test-results/regression-summary.md)
- [Regression Screenshot Evidence](test-evidence/regression/)

## Exploratory Testing & Bug Reporting

I reproduced two issues and wrote Jira-style bug reports.

| Bug ID | Description | Status |
| :-- | :-- | :-- |
| SCRUM-15 | Incorrect product image displayed for Sauce Labs Backpack | To Do |
| SCRUM-17 | Sauce Labs Backpack price changes unexpectedly after refreshing the Products page | To Do |

**Total Reported:** 2

Both issues came from SauceDemo test accounts designed to show problems. They are not confirmed production bugs.

Each bug report includes screenshots and Jira report evidence.

- [SCRUM-15 Bug Report & Evidence](bug-reports/SCRUM-15/bug-report.md)
- [SCRUM-17 Bug Report & Evidence](bug-reports/SCRUM-17/bug-report.md)

## Test Artifacts

### Requirements

- [Derived Functional Requirements, Acceptance Criteria & Test Case Traceability](requirements.md)

### Feature Test Cases

You can view [two sample test cases](test-cases/representative-test-cases.md) on GitHub. The Excel files contain the full test details.

| Feature | Test Cases | Evidence |
| :-- | :-- | :-- |
| Login | [Excel](test-cases/login-test-cases.xlsx) | [Screenshots](test-evidence/login/) |
| Product Listing | [Excel](test-cases/product-test-cases.xlsx) | [Screenshots](test-evidence/product/) |
| Product Details | [Excel](test-cases/product-details-test-cases.xlsx) | [Screenshots](test-evidence/product-details/) |
| Shopping Cart | [Excel](test-cases/cart-test-cases.xlsx) | [Screenshots](test-evidence/cart/) |
| Checkout | [Excel](test-cases/checkout-test-cases.xlsx) | [Screenshots](test-evidence/checkout/) |

### Additional Testing Artifacts

- [E2E Test Cases & Results](test-cases/e2e-test-cases.xlsx)
- [E2E Evidence](test-evidence/e2e/)
- [Regression Testing Summary](test-results/regression-summary.md)
- [Regression Evidence](test-evidence/regression/)
- [Bug Report SCRUM-15](bug-reports/SCRUM-15/bug-report.md)
- [Bug Report SCRUM-17](bug-reports/SCRUM-17/bug-report.md)
- [Test Summary Report](test-results/test-summary-report.md)

This project shows how I practiced writing requirements and test cases, running manual tests, taking screenshots, checking unusual behavior, and reporting results.

The results only cover the tests and environment shown here. Linking test cases to requirements does not mean I tested every SauceDemo feature.
