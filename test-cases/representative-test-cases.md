# Representative Manual QA Test Cases

This browser-friendly page highlights two **existing** test cases from the SauceDemo portfolio. It is a condensed review aid, **not a replacement for the complete Excel test design, test steps, and execution records**. Functional expectations are portfolio-derived rather than official Sauce Labs acceptance criteria.

## TC-CART-005 — Verify the Shopping Cart Displays Added Products

| Field | Detail |
| --- | --- |
| Requirement | `REQ-CART-003` — Cart Product Information |
| Module | Shopping Cart |
| Test Type | Functional — Positive |
| Priority | High |
| Preconditions | The user is logged in and on the Products page. The cart contains one Sauce Labs Backpack and one Sauce Labs Bike Light, with no other products. |
| Execution Status | **PASS** |

**Key steps**

1. Record the names, descriptions, and prices of both products on the Products page.
2. Open the Shopping Cart (`/cart.html`).
3. Confirm that only the two selected products are present.
4. Compare their names, descriptions, prices, and quantities against the Products page.

**Expected:** Backpack is listed at **$29.99**, quantity **1**, and Bike Light at **$9.99**, quantity **1**. Names and descriptions agree with the Products page.

**Observed:** The cart displayed both products at the expected prices and quantities, and their names, descriptions, and prices matched the Products page.

**Supporting artifacts:** [Complete Excel workbook](cart-test-cases.xlsx) · [Products screenshot](../test-evidence/cart/TC-CART-005_PRODUCTS.png) · [Cart screenshot](../test-evidence/cart/TC-CART-005_CART.png)

## TC-CHECKOUT-005 — Verify Order Summary and Price Calculation Accuracy

| Field | Detail |
| --- | --- |
| Requirement | `REQ-CHECKOUT-004` — Order Overview and Totals |
| Module | Checkout & Order Flow |
| Test Type | Manual functional verification |
| Execution Status | **PASS** in the documented regression re-execution |

**Key verification points**

1. In Checkout Overview, compare product names, quantities, and prices with the selected cart items.
2. Check that Payment and Shipping Information is displayed.
3. Verify that **Item Total** equals the sum of item prices and **Total** equals Item Total plus the tax displayed by the application.

**Observed in the documented regression run (2026-10-14):** Backpack **$29.99 × 1** and Bike Light **$9.99 × 1**; Item Total **$39.98**, displayed Tax **$3.20**, and Total **$43.18**. The payment and shipping sections appeared. The calculation matched the displayed amounts.

These amounts are **observed values for this run**, not a claim about an official fixed tax rule.

**Supporting artifacts:** [Complete Excel workbook](checkout-test-cases.xlsx) · [Checkout overview screenshot](../test-evidence/regression/REG-CHECKOUT-005_OVERVIEW.png) · [Regression summary](../test-results/regression-summary.md)

---

For the full execution counts, known limitations, and test conclusion, read the [Manual Test Summary Report](../test-results/test-summary-report.md). Screenshot evidence supports the documented runs; it does not establish coverage of every possible user flow.
