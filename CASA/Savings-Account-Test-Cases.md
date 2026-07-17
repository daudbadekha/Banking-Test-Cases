# 🏦 Savings Account Test Cases

## Module Overview

The Savings Account module allows customers to open, maintain, and manage savings accounts.

---

## Preconditions

- Customer is successfully onboarded.
- Customer KYC is completed.
- User has account opening permission.

---

## Test Cases

| TC ID | Test Scenario | Expected Result |
|--------|---------------|-----------------|
| SA001 | Open savings account with valid customer | Account created successfully |
| SA002 | Open account without KYC | Validation message displayed |
| SA003 | Open account with duplicate account number | Error message displayed |
| SA004 | Minimum deposit validation | Validation should work correctly |
| SA005 | Verify account number generation | Unique account number generated |
| SA006 | Verify nominee addition | Nominee added successfully |
| SA007 | Modify customer address | Address updated successfully |
| SA008 | Close savings account | Account closed successfully |
| SA009 | Search account number | Correct account displayed |
| SA010 | Verify account status | Active account status displayed |

---

## Test Summary

Total Test Cases: **10**

Testing Type: Functional Testing

Module: Savings Account
