# Regression Testing Summary

## Test Objective

The objective of this regression testing exercise is to verify that the Shopping Cart and Checkout functionality continue to work correctly under a simulated change scenario involving Checkout Total Calculation.

This exercise uses a simulated developer fix scenario. No actual code change or deployment was verified.

## Test Environment

- **Application:** SauceDemo
- **URL:** https://www.saucedemo.com/
- **Test Account:** `standard_user`
- **Browser:** Google Chrome
- **Operating System:** Windows 11
- **Execution Date:** 2026-10-14

## Regression Scope

The regression suite focuses on Shopping Cart functionality, checkout price calculation, and successful order completion.

The following existing test cases were selected based on their relevance to the simulated Checkout Total Calculation change.

| TC ID | Test Scenario |
|---|---|
| TC-CART-005 | Verify Shopping Cart Displays Added Products |
| TC-CHECKOUT-005 | Verify Order Summary and Price Calculation Accuracy |
| TC-CHECKOUT-001 | Verify Complete Successful Checkout Flow |

## Test Execution Results

| TC ID | Actual Result | Status | Executed Date |
|---|---|---|---|
| TC-CART-005 | Shopping Cart displayed Sauce Labs Backpack ($29.99) and Sauce Labs Bike Light ($9.99), quantity 1 each. Product information matched the Products page, and Cart Badge displayed 2. | PASS | 2026-10-14 |
| TC-CHECKOUT-005 | Checkout Overview displayed both products with quantity 1 each. Item Total was $39.98, Tax was $3.20, and Total was $43.18. Payment and Shipping Information were displayed correctly. | PASS | 2026-10-14 |
| TC-CHECKOUT-001 | Checkout Overview displayed Sauce Labs Backpack ($29.99), Item Total $29.99, Tax $2.40, and Total $32.39. After clicking Finish, the order confirmation message appeared. Cart Badge had no item count, and the Shopping Cart was empty. | PASS | 2026-10-14 |

### Execution Summary

| Metric | Result |
|---|---:|
| Total Test Cases | 3 |
| Passed | 3 |
| Failed | 0 |
| Blocked | 0 |
| Pass Rate | 100% |

## Evidence

### TC-CART-005 — Shopping Cart

- [Products — Cart Badge](../test-evidence/regression/REG-CART-005_PRODUCTS.png)
- [Shopping Cart — Product Details](../test-evidence/regression/REG-CART-005_CART.png)

### TC-CHECKOUT-005 — Price Calculation

- [Checkout Overview — Order Summary](../test-evidence/regression/REG-CHECKOUT-005_OVERVIEW.png)

### TC-CHECKOUT-001 — Successful Checkout

- [Checkout Overview — Price Calculation](../test-evidence/regression/REG-CHECKOUT-001_OVERVIEW.png)
- [Order Complete — Confirmation](../test-evidence/regression/REG-CHECKOUT-001_COMPLETE.png)
- [Shopping Cart — Empty After Checkout](../test-evidence/regression/REG-CHECKOUT-001_EMPTY_CART.png)

## Conclusion

All 3 selected regression test cases passed.

The Shopping Cart displayed the expected products, quantities, and prices. Checkout calculations matched the expected values, and the order completion process worked successfully.

No failures were observed within the selected regression scope.

**Limitation:** This regression testing was performed as a training exercise based on a simulated Checkout Total Calculation fix. It does not verify an actual developer code change or deployment. The results apply only to the selected scenarios tested on SauceDemo.