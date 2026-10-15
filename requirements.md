# SauceDemo — Derived Functional Requirements

**Document status:** Portfolio reference — all mapped test cases executed  
**Project:** SauceDemo Manual QA Portfolio  
**Application under test:** [https://www.saucedemo.com/](https://www.saucedemo.com/)

> **Important:** These are portfolio-derived requirements based on observed SauceDemo behavior and existing test scenarios. They are **not official specifications from Sauce Labs**. Unconfirmed rules are documented as open questions rather than invented acceptance criteria.

## Scope and Traceability

This document is the single reference for the derived testable behaviors used in this portfolio. `Related Test Cases` refers to the six Excel files in [`test-cases/`](test-cases/). A requirement may link to multiple test cases. All 33 unique test cases have now been executed: **32 Passed and 1 Needs Clarification**. Example prices, product counts, and tax values documented in test runs are observational baselines, not necessarily official business rules.

## 1. Login

### REQ-LOGIN-001 — User Authentication

**Requirement:** The application shall allow valid users to log in and reject invalid login attempts.

**Acceptance Criteria:**

1. Valid credentials open the Products page.
2. Invalid credentials do not grant access and produce an appropriate error message.

**Related Test Cases:** `TC-LOGIN-001`, `TC-LOGIN-002`

### REQ-LOGIN-002 — Required Login Fields

**Requirement:** Username and password are required for login.

**Acceptance Criteria:**

1. Empty username prevents login and shows validation feedback.
2. Empty password prevents login and shows validation feedback.
3. Both fields empty prevent login and show validation feedback.

**Related Test Cases:** `TC-LOGIN-003`, `TC-LOGIN-004`, `TC-LOGIN-005`

### REQ-LOGIN-003 — Account and Page Access Restrictions

**Requirement:** The application shall block locked-out accounts and unauthenticated access to protected Products pages.

**Acceptance Criteria:**

1. Locked-out accounts cannot log in and receive an error.
2. Direct access to the Products page without authentication is denied with appropriate feedback.

**Related Test Cases:** `TC-LOGIN-006`, `TC-LOGIN-007`

### REQ-LOGIN-004 — User Logout

**Requirement:** An authenticated user shall be able to log out and end access to protected pages.

**Acceptance Criteria:**

1. Logout returns the user to the Login page.
2. Protected pages cannot be accessed without logging in again.

**Related Test Cases:** `TC-LOGIN-008`

---

## 2. Product Listing

### REQ-PRODUCT-001 — Product Catalog Display

**Requirement:** The Products page shall show available products and essential product information.

**Acceptance Criteria:**

1. Successful login opens the Products page and product cards are visible.
2. Each displayed product has a non-empty name and a readable numeric price.

**Related Test Cases:** `TC-PRODUCT-001`, `TC-PRODUCT-002`, `TC-PRODUCT-003`

### REQ-PRODUCT-002 — Product Add to Cart Controls

**Requirement:** The catalog shall display Add to cart controls for available products.

**Acceptance Criteria:**

1. Every displayed product in the tested state has an Add to cart button.
2. Buttons have a readable Add to cart label.

**Related Test Cases:** `TC-PRODUCT-004`

### REQ-PRODUCT-003 — Product Price Sorting

**Requirement:** Users shall be able to sort products by ascending price.

**Acceptance Criteria:**

1. Price (Low to High) can be selected.
2. Displayed products are ordered from lowest to highest price.

**Related Test Cases:** `TC-PRODUCT-005`

---

## 3. Product Details

### REQ-DETAIL-001 — Open Product Details

**Requirement:** Users shall be able to open details for a selected product.

**Acceptance Criteria:**

1. Selecting a product opens the corresponding detail page.
2. The page displays the selected product without being blank or showing an error.

**Related Test Cases:** `TC-DETAIL-001`

### REQ-DETAIL-002 — Product Information and Consistency

**Requirement:** Product Details shall display complete and consistent product information.

**Acceptance Criteria:**

1. Name, description, readable price and image are visible.
2. Information matches the corresponding product listing; the image is not broken.

**Related Test Cases:** `TC-DETAIL-002`, `TC-DETAIL-003`

### REQ-DETAIL-003 — Add to Cart from Details

**Requirement:** Users shall be able to add the selected product to the cart from its details page.

**Acceptance Criteria:**

1. Add to cart can be selected on the details page.
2. The selected product is added and reflected in the cart.

**Related Test Cases:** `TC-DETAIL-004`

---

## 4. Shopping Cart

### REQ-CART-001 — Add Products and Update Controls

**Requirement:** Users shall be able to add one or multiple products to the cart.

**Acceptance Criteria:**

1. Single and multiple selected products can be added.
2. Each selected Add to cart button changes to Remove.
3. Unselected product controls remain unchanged.

**Related Test Cases:** `TC-CART-001`, `TC-CART-002`, `TC-CART-003`

### REQ-CART-002 — Cart Badge Count

**Requirement:** The cart badge shall reflect the current item count.

**Acceptance Criteria:**

1. Adding an item increases the count.
2. Removing an item decreases the count.
3. No count is displayed when the cart is empty.

**Related Test Cases:** `TC-CART-004`

### REQ-CART-003 — Cart Product Information

**Requirement:** The cart shall accurately display selected products.

**Acceptance Criteria:**

1. Selected items are shown; unselected items are not.
2. Names, descriptions, prices and quantities correspond to selected products.

**Related Test Cases:** `TC-CART-005`

### REQ-CART-004 — Remove Cart Items

**Requirement:** Users shall be able to remove individual products from the cart.

**Acceptance Criteria:**

1. The selected product is removed.
2. Other products remain and the badge count updates.

**Related Test Cases:** `TC-CART-006`

### REQ-CART-005 — Continue Shopping

**Requirement:** Users shall be able to return to the Products page without losing cart selections.

**Acceptance Criteria:**

1. Continue Shopping opens the Products page.
2. Existing cart items are preserved.

**Related Test Cases:** `TC-CART-007`

---

## 5. Checkout

### REQ-CHECKOUT-001 — Start Checkout

**Requirement:** An authenticated user with items in the cart shall be able to initiate checkout.

**Acceptance Criteria:**

1. Clicking Checkout opens Checkout: Your Information.
2. The purchaser information form is available.

**Related Test Cases:** `TC-CHECKOUT-001`

### REQ-CHECKOUT-002 — Required Purchaser Information

**Requirement:** First Name, Last Name and Postal Code shall be required before continuing.

**Acceptance Criteria:**

1. Missing required fields prevent progression and show appropriate validation feedback.
2. Previously entered values in other fields are retained for tested missing-field cases.
3. Accepted required values allow navigation to Checkout: Overview.

**Related Test Cases:** `TC-CHECKOUT-001`, `TC-CHECKOUT-002`, `TC-CHECKOUT-004`, `TC-CHECKOUT-008`

### REQ-CHECKOUT-003 — Cancel Checkout

**Requirement:** Checkout may be canceled from the information page without losing cart selections.

**Acceptance Criteria:**

1. Cancel returns to the Shopping Cart.
2. Items remain and the cart badge is unchanged.

**Related Test Cases:** `TC-CHECKOUT-003`

### REQ-CHECKOUT-004 — Order Overview and Totals

**Requirement:** Checkout: Overview shall show order details and internally consistent amounts.

**Acceptance Criteria:**

1. Selected products, quantities and prices are correct.
2. Payment and Shipping Information sections appear.
3. Item Total matches selected item amounts; Total equals Item Total plus displayed Tax.

**Related Test Cases:** `TC-CHECKOUT-001`, `TC-CHECKOUT-005`

### REQ-CHECKOUT-005 — Complete Order and Clear Cart

**Requirement:** Users shall be able to finish checkout and have purchased items cleared from the cart.

**Acceptance Criteria:**

1. Finish opens Checkout Complete and displays confirmation.
2. The cart badge count disappears and the revisited cart is empty.

**Related Test Cases:** `TC-CHECKOUT-001`

### REQ-CHECKOUT-006 — Protected Checkout Access

**Requirement:** Unauthenticated users shall not directly access protected checkout pages.

**Acceptance Criteria:**

1. Direct access to Checkout: Your Information is blocked without login.
2. The user is redirected to Login and appropriate feedback is displayed.

**Related Test Cases:** `TC-CHECKOUT-007`

---

## 6. End-to-End Purchase

### REQ-E2E-001 — Complete Purchase Journey

**Requirement:** The application shall support a purchase journey from login to order completion.

**Acceptance Criteria:**

1. User logs in and adds chosen products to the cart.
2. Cart items and quantities match the selection.
3. Accepted information permits checkout, overview totals are consistent and completing the order shows confirmation.

**Related Test Cases:** `TC-E2E-001`

---

## Exploratory Objective — Not a Confirmed Functional Requirement

### EXP-CHECKOUT-001 — Postal Code Special Characters

**Objective:** Observe the response to unusual postal code input, including `@#$%`, and check that the page remains responsive. Record actual behavior without deciding whether special characters should be accepted or rejected.

**Related Test Case:** `TC-CHECKOUT-006` — **Needs Clarification**

**Open Question:** What characters, lengths, and formats should be accepted in Postal Code? The expected business-validation result cannot be confirmed until that rule is specified.

---

## Requirement-to-Test Case Coverage

| Feature | Functional Requirements | Executed Test Cases | Passed | Needs Clarification |
| :-- | --: | --: | --: | --: |
| Login | 4 | 8 | 8 | 0 |
| Product Listing | 3 | 5 | 5 | 0 |
| Product Details | 3 | 4 | 4 | 0 |
| Shopping Cart | 5 | 7 | 7 | 0 |
| Checkout | 6 | 8 (including 1 exploratory) | 7 | 1 |
| End-to-End Purchase | 1 | 1 | 1 | 0 |
| **Total** | **22** | **33** | **32** | **1** |

**Coverage statement:** All 33 executed test-case IDs have been mapped to derived functional requirements or the separately labeled exploratory objective. This is **test-case traceability**, not proof of complete coverage of every SauceDemo feature or formal acceptance of these derived requirements.

### Open Questions and Boundaries

- Postal Code format and character restrictions remain unconfirmed.
- All five additional test cases (`TC-LOGIN-008`, `TC-PRODUCT-005`, `TC-DETAIL-004`, `TC-CART-007`, `TC-CHECKOUT-008`) have been executed and passed.
- Other functionality not included in the test cases (for example, additional sorting options or Back to Products navigation) is outside this document's verified test-case mapping.
- Revisit acceptance criteria if authoritative requirements become available.

## Related Portfolio Files

- [Manual Test Case Workbooks](test-cases/)
- [Test Evidence](test-evidence/)
- [Bug Reports](bug-reports/)
- [Test Results](test-results/)
- [README](README.md)
