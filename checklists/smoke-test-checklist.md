# Smoke Test Checklist — ShopEase

A quick set of critical-path checks run after every new build to confirm core functionality is stable before deeper testing begins.

| # | Check | Status |
|---|---|---|
| 1 | Application loads without errors | ☐ |
| 2 | User can log in with valid credentials | ☐ |
| 3 | User can log out | ☐ |
| 4 | Product search returns results | ☐ |
| 5 | Product detail page opens | ☐ |
| 6 | Item can be added to cart | ☐ |
| 7 | Cart displays correct item count and total | ☐ |
| 8 | Checkout page loads | ☐ |
| 9 | Payment page is reachable | ☐ |
| 10 | No console errors on key pages | ☐ |

**Rule:** If any smoke test fails, the build is rejected and returned to development before further testing.
