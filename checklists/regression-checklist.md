# Regression Test Checklist — ShopEase

Run before each release to confirm existing functionality still works after new changes.

## Authentication
- ☐ Valid login works
- ☐ Invalid login is rejected
- ☐ Logout works
- ☐ Password reset flow works

## Search
- ☐ Keyword search returns correct results
- ☐ Filters apply correctly
- ☐ No-result case handled

## Cart
- ☐ Add to cart works
- ☐ Update quantity recalculates total
- ☐ Remove item works
- ☐ Cart persists after page refresh

## Checkout
- ☐ Order placement succeeds with valid data
- ☐ Payment failure handled gracefully
- ☐ Confirmation email triggered

## Cross-Browser
- ☐ Chrome
- ☐ Firefox
- ☐ Safari
- ☐ Edge
