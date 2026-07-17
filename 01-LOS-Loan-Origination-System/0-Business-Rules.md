# 🏦 Loan Origination System (LOS) - Business Rules

## Purpose

This document defines the business rules applicable during the Loan Origination process. These rules ensure consistency, compliance, and validation before loan approval.

---

# Customer Rules

| Rule ID | Business Rule |
|----------|---------------|
| BR001 | Customer must be registered before applying for a loan. |
| BR002 | Customer KYC must be completed. |
| BR003 | Customer status should be Active. |
| BR004 | Customer should not be blacklisted. |
| BR005 | Customer should not have duplicate Customer IDs. |

---

# Loan Application Rules

| Rule ID | Business Rule |
|----------|---------------|
| BR006 | Loan Product selection is mandatory. |
| BR007 | Loan Amount should be greater than zero. |
| BR008 | Loan Amount must not exceed configured product limit. |
| BR009 | Loan Tenure must be within product configuration. |
| BR010 | Loan Purpose is mandatory. |

---

# Eligibility Rules

| Rule ID | Business Rule |
|----------|---------------|
| BR011 | Customer age should satisfy product policy. |
| BR012 | Monthly income should satisfy eligibility criteria. |
| BR013 | Employment details are mandatory. |
| BR014 | Existing liabilities should be considered during eligibility assessment. |
| BR015 | Debt-to-Income ratio should be within configured policy. |

---

# KYC Rules

| Rule ID | Business Rule |
|----------|---------------|
| BR016 | PAN is mandatory where applicable. |
| BR017 | Aadhaar is mandatory where applicable. |
| BR018 | Mandatory documents should be uploaded. |
| BR019 | Expired documents should not be accepted. |
| BR020 | Unsupported file types should be rejected. |

---

# Document Rules

| Rule ID | Business Rule |
|----------|---------------|
| BR021 | Mandatory documents cannot be skipped. |
| BR022 | Duplicate document uploads should be prevented. |
| BR023 | File size should not exceed configured limit. |
| BR024 | Document approval is required before moving forward. |
| BR025 | Document rejection requires remarks. |

---

# Co-Applicant Rules

| Rule ID | Business Rule |
|----------|---------------|
| BR026 | Relationship with applicant is mandatory. |
| BR027 | PAN should be unique. |
| BR028 | Aadhaar validation should pass. |
| BR029 | KYC should be completed. |
| BR030 | Mandatory fields cannot be blank. |

---

# Guarantor Rules

| Rule ID | Business Rule |
|----------|---------------|
| BR031 | Guarantor details are mandatory if required by the product. |
| BR032 | Guarantor KYC must be completed. |
| BR033 | Guarantor should satisfy minimum age policy. |
| BR034 | Duplicate PAN should not be allowed. |
| BR035 | Income validation should be completed. |

---

# Credit Assessment Rules

| Rule ID | Business Rule |
|----------|---------------|
| BR036 | Income should be verified before assessment. |
| BR037 | Existing loans should be considered. |
| BR038 | Repayment capacity should be calculated. |
| BR039 | Assessment remarks should be saved. |
| BR040 | Only eligible applications proceed to approval. |

---

# Approval Rules

| Rule ID | Business Rule |
|----------|---------------|
| BR041 | Maker cannot approve own application. |
| BR042 | Approval should follow configured hierarchy. |
| BR043 | Only authorized users can approve. |
| BR044 | Approval actions should be audited. |
| BR045 | Fully approved applications proceed to sanction. |

---

# Rejection Rules

| Rule ID | Business Rule |
|----------|---------------|
| BR046 | Rejection remarks are mandatory. |
| BR047 | Unauthorized users cannot reject. |
| BR048 | Rejected applications cannot proceed further. |
| BR049 | Rejection should trigger customer notification (if configured). |
| BR050 | Every rejection should be logged for audit purposes. |

---

# Summary

**Total Business Rules:** 50

**Module:** Loan Origination System (LOS)

**Version:** 1.0
