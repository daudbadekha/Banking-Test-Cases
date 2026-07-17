# 🏦 Current Account Test Cases

## Module Overview

The Current Account module allows businesses and individuals to open and manage current accounts with transaction and overdraft facilities.

---

## Preconditions

- Customer profile exists.
- KYC verification is completed.
- User has permission to open current accounts.

---

## Test Cases

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
|------|---------------|------------|-----------------|----------|
| CA001 | Open current account with valid customer | Enter all mandatory details and submit | Current account should be created successfully | High |
| CA002 | Open account without KYC | Skip KYC details | Validation message displayed | High |
| CA003 | Open account with duplicate customer ID | Use existing customer ID | Duplicate validation displayed | High |
| CA004 | Verify minimum opening balance | Enter balance below minimum | Validation message displayed | High |
| CA005 | Verify account number generation | Open account successfully | Unique account number generated | High |
| CA006 | Add nominee | Enter nominee details | Nominee saved successfully | Medium |
| CA007 | Edit account details | Update communication address | Details updated successfully | Medium |
| CA008 | Close account with zero balance | Close account | Account closed successfully | High |
| CA009 | Close account with pending balance | Attempt closure | Validation message displayed | High |
| CA010 | Search account by account number | Enter account number | Correct account displayed | Medium |
| CA011 | Freeze account | Mark account as frozen | Transactions should not be allowed | High |
| CA012 | Unfreeze account | Remove freeze status | Transactions allowed | Medium |
| CA013 | Verify overdraft eligibility | Enable overdraft | Overdraft activated successfully | Medium |
| CA014 | Verify account status | Open account details | Status displayed correctly | Low |
| CA015 | Verify duplicate account creation | Try creating same account again | Duplicate validation displayed | High |

---

## Test Summary

**Module:** Current Account

**Testing Type:** Functional Testing

**Total Test Cases:** 15
