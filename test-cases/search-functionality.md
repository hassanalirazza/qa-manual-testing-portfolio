# Test Cases — Product Search (ShopEase)

**Module:** Search
**Feature:** Product Search & Filtering

---

### TC_SEARCH_001 — Search with valid keyword

| Field | Value |
|---|---|
| **Priority** | High |
| **Test Data** | Keyword: "headphones" |

**Steps:**
1. Enter "headphones" in the search bar
2. Press Enter

**Expected Result:** Relevant products containing "headphones" are listed with name, price, and image.

---

### TC_SEARCH_002 — Search with no matching results

| Field | Value |
|---|---|
| **Priority** | Medium |
| **Test Data** | Keyword: "xyzqwerty123" |

**Steps:**
1. Enter a keyword with no matches
2. Press Enter

**Expected Result:** A "No results found" message is displayed with suggestions to refine the search.

---

### TC_SEARCH_003 — Search is case-insensitive

| Field | Value |
|---|---|
| **Priority** | Medium |
| **Test Data** | "LAPTOP" vs "laptop" |

**Steps:**
1. Search "LAPTOP"
2. Search "laptop"

**Expected Result:** Both searches return the same set of results.

---

### TC_SEARCH_004 — Filter results by price range

| Field | Value |
|---|---|
| **Priority** | Medium |
| **Test Data** | Price range: $50–$100 |

**Steps:**
1. Search for a product category
2. Apply the price filter $50–$100

**Expected Result:** Only products priced between $50 and $100 are shown.

---

### TC_SEARCH_005 — Empty search submission

| Field | Value |
|---|---|
| **Priority** | Low |

**Steps:**
1. Leave the search bar empty
2. Press Enter

**Expected Result:** No search is performed, or the user is prompted to enter a keyword. No errors occur.
