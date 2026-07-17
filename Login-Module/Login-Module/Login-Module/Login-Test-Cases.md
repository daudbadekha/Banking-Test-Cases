# 🏦 Login Module Test Cases

## Module Overview

The Login Module is responsible for authenticating users and providing secure access to the banking application.

---

## Preconditions

- User is registered in the banking system.
- User has a valid username and password.
- Banking application is available.
- Internet connection is active.

---

## Test Cases

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
|------|----------------|------------|-----------------|----------|
| LGN001 | Login with valid username and password | Enter valid credentials and click Login | User should be redirected to Dashboard | High |
| LGN002 | Login with invalid password | Enter valid username and incorrect password | Appropriate error message should be displayed | High |
| LGN003 | Login with invalid username | Enter invalid username and valid password | Appropriate error message should be displayed | High |
| LGN004 | Login with blank username | Leave username empty and click Login | Username validation message should appear | Medium |
| LGN005 | Login with blank password | Leave password empty and click Login | Password validation message should appear | Medium |
| LGN006 | Login with both fields blank | Leave both fields empty | Mandatory field validation messages should appear | High |
| LGN007 | Verify password masking | Type password | Password characters should be masked | Medium |
| LGN008 | Verify Forgot Password link | Click Forgot Password | Password reset page should open | Medium |
| LGN009 | Verify Logout functionality | Click Logout after successful login | User should be logged out and redirected to Login page | High |
| LGN010 | Verify session timeout | Keep application idle for configured timeout | User session should expire and Login page should be displayed | Medium |

---

## Test Summary

- Total Test Cases: **10**
- Module: **Login**
- Testing Type: **Functional Testing**
- Domain: **Banking**
