
# SauceDemo Manual Testing

## Project Overview

SauceDemo is a demo e-commerce website created by
Sauce Labs for software testing practice.

This project focuses on practicing manual testing
using real-world QA workflows.

The main objectives are to design test scenarios,
create test cases, execute tests, verify actual
results against expected results, and document
testing outcomes.

The project covers key e-commerce features,
including Login, Product Listing, Product Details,
Shopping Cart, and Checkout.

Testing will be performed step by step, starting
with Login and continuing through the main shopping flow.

This project also aims to improve practical QA testing skills.

## Test Scope

### Completed

**Login**
- Valid Login
- Invalid Password
- Empty Username
- Empty Password
- Empty Username and Password
- Unauthorized Access to Products Page
- Locked Account Login

**Execution Results:** 7 Passed, 0 Failed


**Product Listing**
- Verify Product Listing After Successful Login
- Verify Product Names Are Displayed
- Verify Product Prices Are Displayed
- Verify Add to Cart Buttons Are Displayed

**Execution Results:** 4 Passed, 0 Failed


**Product Details**

- Verify Product Details Page Opens
- Verify Product Details Information Is Displayed
- Verify Product Details Match the Selected Product

**Execution Results:** 3 Passed, 0 Failed


**Shopping Cart**

- Verify Adding a Product to Cart
- Verify Adding Multiple Products to Cart
- Verify Add to Cart Button Changes to Remove
- Verify Cart Badge Updates Correctly
- Verify Shopping Cart Displays Added Products
- Verify Removing Products from Shopping Cart

**Execution Results:** 6 Passed, 0 Failed


**Checkout & Order Flow**

- Verify Complete Successful Checkout Flow
- Verify Checkout with Empty First Name
- Verify Cancel from Checkout Information Page
- Verify Checkout with Empty Last Name
- Verify Order Summary and Price Calculation Accuracy
- Verify Postal Code Input with Special Characters
- Verify Unauthenticated Checkout Access

**Execution Results:** 6 Passed, 0 Failed, 1 Needs Clarification


**Exploratory Testing & Jira Bug Reporting**

- SCRUM-15: Incorrect product image displayed for Sauce Labs Backpack
- SCRUM-17: Sauce Labs Backpack price changes unexpectedly after refreshing Products page

**Defects Reported:** 2
**Status:** To Do (Open)

Both defects were reproduced using fault-injected
test accounts in the SauceDemo demo application.
They are not production defects.

### Planned

- End-to-End and Regression Testing
- Final Manual QA Portfolio Review

## Testing Approach

- **Manual Testing:** Execute test cases manually using a web browser.
- **Positive Testing:** Verify that users can log in with valid credentials.
- **Negative Testing:** Verify that the system rejects invalid login attempts.
- **Input Validation Testing:** Test empty username and password fields.
- **Authorization Testing:** Verify that unauthenticated users cannot access protected pages.
- **Account Status Testing:** Verify that locked accounts cannot log in.
- **Result Verification:** Compare actual results with expected results and record PASS/FAIL.

## Test Artifacts

- [Login Test Cases](test-cases/login-test-cases.xlsx)
- [Login Test Evidence](test-evidence/login/)
- [Product Test Cases](test-cases/product-test-cases.xlsx)
- [Product Test Evidence](test-evidence/product/)
- [Product Details Test Cases](test-cases/product-details-test-cases.xlsx)
- [Product Details Evidence](test-evidence/product-details/)
- [Shopping Cart Test Cases](test-cases/cart-test-cases.xlsx)
- [Shopping Cart Test Evidence](test-evidence/cart/)
- [Checkout Test Cases](test-cases/checkout-test-cases.xlsx)
- [Checkout Test Evidence](test-evidence/checkout/)
- [Bug Report SCRUM-15](bug-reports/SCRUM-15/)
- [Bug Report SCRUM-17](bug-reports/SCRUM-17/)