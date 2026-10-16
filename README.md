# SauceDemo Manual Testing Portfolio

## Project Overview

This project demonstrates a practical manual QA testing workflow using [SauceDemo](https://www.saucedemo.com/), a demo e-commerce application provided by Sauce Labs.

The project covers requirement analysis, test case design, test execution, result verification, defect reporting, end-to-end testing, and regression testing.

- **Application Under Test:** SauceDemo
- **Testing Type:** Manual Testing
- **Test Environment:** Google Chrome, Windows 11
- **Test Management:** Excel
- **Defect Reporting:** Jira-style reports and documented Jira evidence
- **Requirements:** [Portfolio-Derived Functional Requirements](requirements.md)

> **Requirements note:** The requirements used in this portfolio are derived from observed application behavior and the documented test scenarios. They are not official business specifications provided by Sauce Labs.

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

All 33 unique test cases have been executed. The totals include one end-to-end test case and one exploratory checkout test case.

**Clarification note:** `TC-CHECKOUT-006` uses special characters in the Postal Code field. The application accepted the input, but there is no confirmed business rule defining the permitted format. The result is therefore **Needs Clarification**, not a confirmed functional failure or pass against a postal-code validation rule.

## Testing Approach

The following testing approaches were applied:

- **Requirement Analysis:** Used portfolio-derived requirements and acceptance criteria to connect test scenarios to expected behavior.
- **Functional Testing:** Verified core e-commerce features against documented expected results.
- **Positive Testing:** Tested valid user actions and successful workflows.
- **Negative Testing:** Tested invalid inputs, missing required fields, and restricted access.
- **Input Validation Testing:** Checked required fields and observed application behavior for selected input conditions.
- **Access Control Testing:** Checked whether unauthenticated users could access protected pages.
- **End-to-End Testing:** Verified a complete purchase journey from login through order confirmation.
- **Regression Testing:** Re-executed selected existing test cases under a simulated change scenario.
- **Exploratory Testing:** Investigated unexpected application behavior and documented reproducible issues.

Actual results, execution status, and screenshot evidence are recorded in the test case workbooks. Test cases include a `Requirement ID` that links to [requirements.md](requirements.md).


Evidence screenshots are organized by Test Case ID and support the overall execution result. They are not necessarily mapped one-to-one to individual Actual Result entries.


## End-to-End Testing

One end-to-end test case was designed and executed to verify the complete purchase flow.

**TC-E2E-001 — End-to-End Purchase Flow with Two Products**

The scenario covers:

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

Regression testing was performed as a training exercise under a **simulated developer fix scenario** involving Checkout Total Calculation.

Three existing test cases were selected and re-executed to check Shopping Cart and Checkout behavior.

| Test Case ID | Scenario | Status |
| :-- | :-- | :-- |
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
| :-- | :-- | :-- |
| SCRUM-15 | Incorrect product image displayed for Sauce Labs Backpack | To Do |
| SCRUM-17 | Sauce Labs Backpack price changes unexpectedly after refreshing the Products page | To Do |

**Total Reported:** 2

Both issues were observed using fault-injected test accounts provided by SauceDemo. They should not be interpreted as production defects.

Bug report evidence includes screenshots of the observed behavior and Jira reports.

- [SCRUM-15 Bug Report & Evidence](bug-reports/SCRUM-15/bug-report.md)
- [SCRUM-17 Bug Report & Evidence](bug-reports/SCRUM-17/bug-report.md)

## Test Artifacts

### Requirements

- [Derived Functional Requirements, Acceptance Criteria & Test Case Traceability](requirements.md)

### Feature Test Cases

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

## Overall Results

| Category | Result |
| :-- | :-- |
| Feature Test Cases | 32 total — 31 Passed, 1 Needs Clarification |
| E2E Test Cases | 1 Passed |
| **All Unique Test Cases** | **33 total — 32 Passed, 1 Needs Clarification** |
| Regression Re-executions | 3 Passed (not additional unique cases) |
| Exploratory Bug Reports | 2 documented issues using fault-injected accounts |

This portfolio demonstrates the process of analyzing testable requirements, designing and executing manual tests, collecting evidence, investigating unexpected behavior, and reporting results.

The reported results are limited to the scenarios and test environments documented in this repository. Test-case traceability does not establish complete coverage of every SauceDemo feature.
