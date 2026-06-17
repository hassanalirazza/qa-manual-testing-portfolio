# Test Cases — Checkout Flow (ShopEase)

**Module:** Checkout
**Feature:** Cart & Order Placement

---

### TC_CHECKOUT_001 — Place order with single item

| Field | Value |
|---|---|
| **Priority** | High |
| **Preconditions** | User is logged in; one item is in the cart |
| **Test Data** | Item: "Wireless Mouse" / Qty: 1 |

**Steps:**
1. Open the cart
2. Click **Proceed to Checkout**
3. Enter a valid shipping address
4. Select a payment method
5. Click **Place Order**

**Expected Result:** Order is placed successfully. An order confirmation number is displayed and a confirmation email is triggered.

---

### TC_CHECKOUT_002 — Update item quantity in cart

| Field | Value |
|---|---|
| **Priority** | High |
| **Preconditions** | User is logged in; one item is in the cart |
| **Test Data** | Qty changed from 1 to 3 |

**Steps:**
1. Open the cart
2. Change the item quantity to 3
3. Observe the order total

**Expected Result:** Line total and order total recalculate correctly to reflect quantity 3.

---

### TC_CHECKOUT_003 — Remove item from cart

| Field | Value |
|---|---|
| **Priority** | Medium |
| **Preconditions** | User is logged in; two items are in the cart |

**Steps:**
1. Open the cart
2. Click **Remove** on one item

**Expected Result:** The item is removed. Cart count and total update accordingly. The other item remains.

---

### TC_CHECKOUT_004 — Checkout with empty cart

| Field | Value |
|---|---|
| **Priority** | Medium |
| **Preconditions** | User is logged in; cart is empty |

**Steps:**
1. Navigate directly to the checkout page

**Expected Result:** System prevents checkout. A message "Your cart is empty" is shown with a link back to products.

---

### TC_CHECKOUT_005 — Order fails on declined payment

| Field | Value |
|---|---|
| **Priority** | High |
| **Preconditions** | User is logged in; valid item in cart |
| **Test Data** | Test card that simulates a decline |

**Steps:**
1. Proceed to checkout
2. Enter the declined test card details
3. Click **Place Order**

**Expected Result:** Order is not placed. A clear payment failure message is shown. The cart contents are preserved.
