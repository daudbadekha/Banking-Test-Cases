# 🏦 Account Closure Test Cases

## Module Overview

This module verifies the account closure process for Savings and Current Accounts.

---

## Preconditions

- Customer account exists.
- User has account closure permission.
- Account details are accessible.

---

## Test Cases

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
|------|---------------|------------|-----------------|----------|
| AC001 | Close active account with zero balance | Select account and click Close | Account closed successfully | High |
| AC002 | Close account with available balance | Attempt closure | Validation message displayed | High |
| AC003 | Close account with pending transactions | Attempt closure | Closure should not be allowed | High |
| AC004 | Close account without selecting reason | Leave reason blank | Validation message displayed | Medium |
| AC005 | Close already closed account | Attempt closure | Appropriate error message displayed | Medium |
| AC006 | Verify closure date | Close account | Current date should be recorded | Medium |
| AC007 | Verify audit trail | Close account | Closure action logged | High |
| AC008 | Verify customer notification | Close account | Notification generated | Low |
| AC009 | Verify account search after closure | Search closed account | Status displayed as Closed | Medium |
| AC010 | Verify closure remarks | Enter remarks and save | Remarks stored successfully | Low |
| AC011 | Verify authorization requirement | Maker submits closure | Checker approval required | High |
| AC012 | Reject closure request | Checker rejects request | Account remains Active | High |
| AC013 | Approve closure request | Checker approves | Account status updated to Closed | High |
| AC014 | Verify closure report | Generate report | Closed account appears in report | Medium |
| AC015 | Attempt transaction on closed account | Perform deposit | Transaction should not be allowed | High |

---

## Test Summary

**Module:** Account Closure

**Testing Type:** Functional Testing

**Total Test Cases:** 15
