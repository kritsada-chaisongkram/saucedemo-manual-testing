# SauceDemo Manual Testing Portfolio

## Project Overview

This project demonstrates a practical manual QA testing workflow using [SauceDemo](https://www.saucedemo.com/), a demo e-commerce application provided by Sauce Labs.

The project covers test case design, test execution, result verification, defect reporting, end-to-end testing, and regression testing.

- **Application Under Test:** SauceDemo
- **Testing Type:** Manual Testing
- **Test Environment:** Google Chrome, Windows 11
- **Test Management:** Excel
- **Defect Reporting:** Jira

## Test Scope & Execution Summary

| Feature | Total Test Cases | Passed | Failed | Needs Clarification |
|---|---:|---:|---:|---:|
| Login | 7 | 7 | 0 | 0 |
| Product Listing | 4 | 4 | 0 | 0 |
| Product Details | 3 | 3 | 0 | 0 |
| Shopping Cart | 6 | 6 | 0 | 0 |
| Checkout & Order Flow | 7 | 6 | 0 | 1 |
| **Total** | **27** | **26** | **0** | **1** |

**Note:** The checkout postal code test using special characters was marked as *Needs Clarification* because the application accepted the input, but no confirmed business requirement was available to determine whether this behavior was correct.

## Testing Approach

The following testing approaches were applied:

- **Functional Testing:** Verified core e-commerce features against expected results.
- **Positive Testing:** Tested valid user actions and successful workflows.
- **Negative Testing:** Tested invalid inputs, missing required fields, and restricted access.
- **Input Validation Testing:** Checked required fields and observed application behavior for selected input conditions.
- **Access Control Testing:** Checked whether unauthenticated users could access protected pages.
- **End-to-End Testing:** Verified a complete purchase journey from login through order confirmation.
- **Regression Testing:** Re-executed selected existing test cases under a simulated change scenario.
- **Exploratory Testing:** Investigated unexpected application behavior and documented reproducible issues.

Actual results, execution status, and screenshot evidence were recorded for the executed test cases.

## End-to-End Testing

One end-to-end test case was designed and executed to verify the complete purchase flow.

**TC-E2E-001 — End-to-End Purchase Flow with Two Products**

The scenario covers:

1. Login with a valid user account
2. Select and add two products to the cart
3. Verify cart contents
4. Enter checkout information
5. Verify order summary and price calculation
6. Complete the order and verify confirmation

**Execution Result:** 1 Passed, 0 Failed

- [E2E Test Cases & Execution Results](test-cases/e2e-test-cases.xlsx)
- [E2E Screenshot Evidence](test-evidence/e2e/)

## Regression Testing

Regression testing was performed as a training exercise under a **simulated developer fix scenario** involving Checkout Total Calculation.

Three existing test cases were selected and re-executed to check Shopping Cart and Checkout behavior.

| Test Case ID | Scenario | Status |
|---|---|---|
| TC-CART-005 | Shopping Cart Displays Added Products | PASS |
| TC-CHECKOUT-005 | Order Summary and Price Calculation Accuracy | PASS |
| TC-CHECKOUT-001 | Complete Successful Checkout Flow | PASS |

**Execution Result:** 3 Passed, 0 Failed

These are re-executions of existing test cases and are not counted as additional unique test cases in the main execution summary.

**Limitation:** This exercise does not verify an actual code change or deployment.

- [Regression Testing Summary](test-results/regression-summary.md)
- [Regression Screenshot Evidence](test-evidence/regression/)

## Exploratory Testing & Bug Reporting

Two issues were reproduced and documented using Jira-style bug reports.

| Bug ID | Description | Status |
|---|---|---|
| SCRUM-15 | Incorrect product image displayed for Sauce Labs Backpack | To Do |
| SCRUM-17 | Sauce Labs Backpack price changes unexpectedly after refreshing the Products page | To Do |

**Total Reported:** 2

Both issues were observed using fault-injected test accounts provided by SauceDemo. They should not be interpreted as production defects.

Bug report evidence includes screenshots of the observed behavior and Jira reports.

- [SCRUM-15 Bug Report & Evidence](bug-reports/SCRUM-15/bug-report.md)
- [SCRUM-17 Bug Report & Evidence](bug-reports/SCRUM-17/bug-report.md)
## Test Artifacts

### Functional Test Cases

| Feature | Test Cases | Evidence |
|---|---|---|
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
- [Bug Report SCRUM-15](bug-reports/SCRUM-15/)
- [Bug Report SCRUM-17](bug-reports/SCRUM-17/)

## Overall Results

| Category | Result |
|---|---|
| Functional Test Cases | 27 total — 26 Passed, 1 Needs Clarification |
| E2E Test Cases | 1 Passed |
| Regression Re-executions | 3 Passed |
| Exploratory Bug Reports | 2 documented issues |

The project demonstrates the process of designing test cases, performing manual test execution, collecting evidence, investigating unexpected behavior, and reporting testing results.

The reported results are limited to the scenarios and test environments documented in this repository.