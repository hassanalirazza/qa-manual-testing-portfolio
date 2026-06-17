# Test Cases — Login Functionality (ShopEase)

**Module:** Authentication
**Feature:** User Login

---

### TC_LOGIN_001 — Valid login with correct credentials

| Field | Value |
|---|---|
| **Priority** | High |
| **Preconditions** | User is registered and on the login page |
| **Test Data** | Email: `user@shopease.com` / Password: `Valid@123` |

**Steps:**
1. Enter a valid email in the Email field
2. Enter the correct password in the Password field
3. Click the **Login** button

**Expected Result:** User is authenticated and redirected to the dashboard. A welcome message displays the user's name.

---

### TC_LOGIN_002 — Login with invalid password

| Field | Value |
|---|---|
| **Priority** | High |
| **Preconditions** | User is registered and on the login page |
| **Test Data** | Email: `user@shopease.com` / Password: `Wrong@999` |

**Steps:**
1. Enter a valid email
2. Enter an incorrect password
3. Click the **Login** button

**Expected Result:** Login is rejected. An error message "Invalid email or password" is displayed. User remains on the login page.

---

### TC_LOGIN_003 — Login with empty fields

| Field | Value |
|---|---|
| **Priority** | Medium |
| **Preconditions** | User is on the login page |
| **Test Data** | Email: (blank) / Password: (blank) |

**Steps:**
1. Leave both fields empty
2. Click the **Login** button

**Expected Result:** Inline validation messages appear for both required fields. No request is sent to the server.

---

### TC_LOGIN_004 — Email format validation

| Field | Value |
|---|---|
| **Priority** | Medium |
| **Preconditions** | User is on the login page |
| **Test Data** | Email: `user.shopease.com` / Password: `Valid@123` |

**Steps:**
1. Enter an email without the `@` symbol
2. Enter any password
3. Click the **Login** button

**Expected Result:** A validation message "Please enter a valid email address" is displayed. Login is not attempted.

---

### TC_LOGIN_005 — Account lockout after repeated failures

| Field | Value |
|---|---|
| **Priority** | High |
| **Preconditions** | User is registered |
| **Test Data** | Valid email + incorrect password |

**Steps:**
1. Enter a valid email with an incorrect password
2. Repeat the failed login attempt 5 times

**Expected Result:** After 5 failed attempts, the account is temporarily locked. A message indicates the lockout and suggested wait time.
