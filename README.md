
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

### Planned

- Product Details
- Add to Cart and Shopping Cart
- Checkout and Order Flow
- End-to-End and Regression Testing

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