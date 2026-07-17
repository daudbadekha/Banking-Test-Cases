# 🏦 Customer Onboarding Test Cases

## Module Overview

The Customer Onboarding module allows the bank to register new customers, validate KYC details, and create customer records before account opening.

---

## Preconditions

- User has permission to create customers.
- Customer onboarding screen is accessible.
- Mandatory KYC documents are available.
- Application is connected to the database.

---

## Test Cases

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
|------|---------------|------------|-----------------|----------|
| CUST001 | Create customer with all valid details | Enter all mandatory information and submit | Customer record should be created successfully | High |
| CUST002 | Leave First Name blank | Do not enter First Name | Validation message should appear | High |
| CUST003 | Leave Mobile Number blank | Do not enter Mobile Number | Validation message should appear | High |
| CUST004 | Enter invalid Mobile Number | Enter fewer than 10 digits | Error message displayed | Medium |
| CUST005 | Enter invalid Email Address | Enter invalid email format | Validation message displayed | Medium |
| CUST006 | Select invalid Date of Birth | Enter a future date | Validation message displayed | Medium |
| CUST007 | Duplicate PAN Number | Enter an existing PAN | Duplicate customer validation should appear | High |
| CUST008 | Duplicate Aadhaar Number | Enter an existing Aadhaar number | Duplicate validation should appear | High |
| CUST009 | Upload unsupported document format | Upload an unsupported file type | Error message displayed | Medium |
| CUST010 | Upload oversized document | Upload file exceeding limit | Validation message displayed | Medium |
| CUST011 | Save customer successfully | Complete all mandatory fields and submit | Customer ID should be generated | High |
| CUST012 | Cancel customer creation | Click Cancel before saving | Data should not be saved | Low |
| CUST013 | Search newly created customer | Search using Customer ID | Customer details should be displayed | High |
| CUST014 | Edit customer details | Modify address and save | Updated details should be saved | Medium |
| CUST015 | Verify mandatory KYC validation | Skip mandatory KYC document | Validation message displayed | High |

---

## Test Summary

- Total Test Cases: **15**
- Module: **Customer Onboarding**
- Testing Type: **Functional Testing**
- Domain: **Banking**
