# 🏦 Loan Application - Functional Test Cases

## Module Overview

This document contains functional test cases for the Loan Application process in a Loan Origination System (LOS). The scenarios cover data validation, business rules, customer eligibility, workflow, and loan submission.

---

# Preconditions

- Customer profile exists.
- Customer KYC is completed.
- User has permission to create loan applications.
- Loan products are configured.
- Branch is active.

---

# Test Cases

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
|------|---------------|------------|-----------------|----------|
| LOS001 | Create loan application with valid customer | Enter valid customer details and submit | Loan application created successfully | High |
| LOS002 | Submit application without Customer ID | Leave Customer ID blank | Validation message displayed | High |
| LOS003 | Submit application without Loan Product | Leave Loan Product blank | Mandatory field validation | High |
| LOS004 | Enter invalid Loan Amount | Enter negative value | Validation message displayed | High |
| LOS005 | Enter Loan Amount above configured limit | Enter amount exceeding limit | Validation message displayed | High |
| LOS006 | Select invalid Loan Purpose | Choose unsupported purpose | Error displayed | Medium |
| LOS007 | Leave Employment Type blank | Skip Employment Type | Validation message displayed | High |
| LOS008 | Leave Income field blank | Skip Monthly Income | Validation displayed | High |
| LOS009 | Enter invalid Mobile Number | Enter fewer than 10 digits | Validation displayed | Medium |
| LOS010 | Submit duplicate application | Create second application for same request | Duplicate validation displayed | High |
| LOS011 | Save application as Draft | Click Save Draft | Draft saved successfully | Medium |
| LOS012 | Submit completed application | Fill all mandatory fields | Application submitted successfully | High |
| LOS013 | Cancel application before submission | Click Cancel | Data not saved | Low |
| LOS014 | Verify generated Application Number | Submit application | Unique Application Number generated | High |
| LOS015 | Verify audit trail | Submit application | Activity logged successfully | Medium |
| LOS016 | Verify mandatory remarks during rejection | Reject without remarks | Validation message displayed | Medium |
| LOS017 | Verify co-applicant addition | Add valid co-applicant | Co-applicant linked successfully | Medium |
| LOS018 | Verify guarantor addition | Add guarantor | Guarantor linked successfully | Medium |
| LOS019 | Verify unsupported file upload | Upload unsupported document | Validation message displayed | Medium |
| LOS020 | Verify successful application submission | Submit complete application | Status updated to Submitted | High |

---

# Validation Checklist

- Customer ID mandatory
- Loan Product mandatory
- Loan Amount mandatory
- Income mandatory
- Employment details mandatory
- Mobile Number validation
- Email validation
- Document validation
- Duplicate application validation
- Loan limit validation

---

# Exit Criteria

- All mandatory validations passed.
- Loan Application Number generated.
- Application status updated successfully.
- Audit logs created.
