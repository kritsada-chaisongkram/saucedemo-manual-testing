# SauceDemo — Manual Test Summary Report

**Project:** SauceDemo Manual QA Portfolio  
**Application Under Test:** [SauceDemo](https://www.saucedemo.com/)  
**Report Date:** 2026-10-16  
**Test Type:** Manual Testing  
**Environment:** Google Chrome, Windows 11  
**Test Management:** Excel; Jira-style defect reports  
**Execution Status:** Completed for the documented scope, with one requirement clarification outstanding

> **Portfolio context:** This report summarizes a testing exercise on a demo application. The functional requirements are derived from observed behavior and test scenarios, not official Sauce Labs specifications. This report is not a production release sign-off.

## 1. Test Objective and Scope

The objective was to assess the documented SauceDemo e-commerce workflows, record observed results, provide reproducible evidence, and communicate issues and residual risks.

**In scope:** Login and logout, Product Listing, Product Details, Shopping Cart, Checkout and Order Flow, and one End-to-End Purchase scenario. Testing included positive, negative, access-control, input-validation, and exploratory scenarios. A targeted regression exercise was also conducted separately.

**Scope limitation:** The results cover the scenarios and environment documented in this portfolio only. They do not establish complete coverage of SauceDemo or confirm production release readiness.

## 2. Test Execution Summary

| Feature | Executed | Passed | Failed | Needs Clarification |
| :-- | --: | --: | --: | --: |
| Login | 8 | 8 | 0 | 0 |
| Product Listing | 5 | 5 | 0 | 0 |
| Product Details | 4 | 4 | 0 | 0 |
| Shopping Cart | 7 | 7 | 0 | 0 |
| Checkout & Order Flow | 8 | 7 | 0 | 1 |
| End-to-End Purchase | 1 | 1 | 0 | 0 |
| **Total unique test cases** | **33** | **32** | **0** | **1** |

**Execution completion:** All 33 unique test cases were executed. Of these, 32 passed, none had a confirmed failure under the documented expectations, and one remains **Needs Clarification**. The latter must not be counted as a pass or a fail.

The test cases map to **22 portfolio-derived functional requirements** and **one separately identified exploratory objective**. See the [Requirements and Traceability document](../requirements.md) and [Test Case Workbooks](../test-cases/).

## 3. End-to-End and Regression Results

| Activity | Result | Interpretation |
| :-- | :-- | :-- |
| E2E purchase journey (`TC-E2E-001`) | 1 Passed | Included among the 33 unique cases above |
| Targeted regression re-executions | 3 Passed, 0 Failed | Existing cases re-run; **not** three additional unique test cases |

The E2E case covered login, selection of two products, cart verification, checkout information, order totals, and order confirmation. See [E2E Test Cases](../test-cases/e2e-test-cases.xlsx) and [E2E Evidence](../test-evidence/e2e/).

The regression exercise focused on `TC-CART-005`, `TC-CHECKOUT-005`, and `TC-CHECKOUT-001` under a **simulated developer fix** related to Checkout Total Calculation. **No actual code fix or deployment was verified.** See the [Regression Testing Summary](regression-summary.md).

## 4. Defect Summary

Two reproducible issues were documented using **fault-injected SauceDemo test accounts**. They demonstrate bug investigation and reporting; they are **not confirmed production defects**.

| Bug ID | Observed Issue | Account | Severity | Priority | Documented Status |
| :-- | :-- | :-- | :-- | :-- | :-- |
| [SCRUM-15](../bug-reports/SCRUM-15/bug-report.md) | Incorrect image for Sauce Labs Backpack | `problem_user` | Medium | Medium | To Do |
| [SCRUM-17](../bug-reports/SCRUM-17/bug-report.md) | Backpack listing price varies after page refresh while other pages show $29.99 | `visual_user` | Medium | High | To Do |

Both reports contain reproduction steps, expected and actual behavior, and screenshot evidence. These two issues are tracked separately from the 33-case execution summary and should not be presented as failures found in the standard user test run.

## 5. Open Questions, Risks, and Limitations

- **Unconfirmed postal-code rule:** `TC-CHECKOUT-006` observed that the Postal Code field accepted special characters (`@#$%`). Without a confirmed rule on permitted characters or format, the result remains **Needs Clarification** rather than a confirmed pass or defect.
- **Limited coverage:** Additional sorting modes, other navigation paths, and untested workflows are outside the documented scope. The derived requirement-to-test mapping is traceability, not evidence of complete product coverage.
- **Regression simulation:** The targeted regression run did not validate an actual change or deployment.
- **Fault-injected accounts:** `SCRUM-15` and `SCRUM-17` describe intentionally problematic demo-account behavior, so they must not be interpreted as production defects.

## 6. Test Conclusion and Recommendation

**Conclusion:** The documented manual testing scope is complete: **33 unique cases executed, 32 passed, 0 confirmed failed, and 1 awaiting requirement clarification**. The selected E2E scenario passed, and the three targeted regression re-executions passed within their simulated-change context.

**Recommendation:** The portfolio test cycle can be closed with the postal-code question explicitly recorded as unresolved. If this were a real release decision, confirm the postal-code acceptance criteria with the Product Owner or Business Analyst and assess any resulting retest needs before sign-off. No production release approval is implied by these results.

## 7. Supporting Artifacts

- [Project README](../README.md)
- [Derived Functional Requirements and Test Case Traceability](../requirements.md)
- [Feature Test Case Workbooks and Execution Results](../test-cases/)
- [Screenshot Evidence](../test-evidence/)
- [Regression Testing Summary](regression-summary.md)
- [Bug Report SCRUM-15](../bug-reports/SCRUM-15/bug-report.md)
- [Bug Report SCRUM-17](../bug-reports/SCRUM-17/bug-report.md)

**Evidence organization:** Screenshots are grouped by Test Case ID and support the overall execution result; they are not necessarily mapped one-to-one to individual Actual Result entries.
