# Login Module Test Cases

## Module
Login & Authentication

---

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
|------|---------------|------------|-----------------|----------|
| TC001 | Login with valid username and password | Enter valid credentials and click Login | User should be logged in successfully | High |
| TC002 | Login with invalid password | Enter valid username and incorrect password | Error message should be displayed | High |
| TC003 | Login with invalid username | Enter invalid username and valid password | Error message should be displayed | High |
| TC004 | Login with blank username | Leave username empty | Validation message should appear | Medium |
| TC005 | Login with blank password | Leave password empty | Validation message should appear | Medium |
| TC006 | Login with both fields blank | Leave username and password empty | Mandatory field validation should appear | High |
| TC007 | Verify password masking | Enter password | Password should be masked | Medium |
| TC008 | Verify Forgot Password link | Click Forgot Password | Password recovery page should open | Medium |
| TC009 | Verify Logout | Click Logout | User should be logged out successfully | High |
| TC010 | Verify session timeout | Keep session idle | User should be logged out after timeout | Medium |

---

**Prepared For:** Practice & Portfolio

**Domain:** Banking

**Testing Type:** Functional Testing
