# 🏦 Customer Eligibility - Functional Test Cases

## Document Information

| Field | Value |
|-------|-------|
| Module | Loan Origination System (LOS) |
| Feature | Customer Eligibility |
| Testing Type | Functional Testing |
| Version | 1.0 |
| Author | Daud Badekha |
| Last Updated | July 2026 |

---

# Objective

To verify that the system correctly evaluates customer eligibility based on business rules before allowing loan processing.

---

# Preconditions

- Customer profile exists.
- KYC is completed.
- Loan Product is configured.
- User is logged into LOS.
- Customer has provided income and employment details.

---

# Test Cases

| TC ID | Requirement ID | Module | Preconditions | Test Scenario | Test Steps | Test Data | Expected Result | Priority | Test Type |
|------|----------------|---------|--------------|--------------|------------|-----------|-----------------|----------|-----------|
| ELG001 | LOS-REQ-101 | Eligibility | Customer exists | Verify eligibility for salaried customer | Select salaried customer | Salary ₹50,000 | Customer eligible | High | Positive |
| ELG002 | LOS-REQ-102 | Eligibility | Customer exists | Verify eligibility for self-employed customer | Select self-employed | Business Income ₹1,20,000 | Customer eligible | High | Positive |
| ELG003 | LOS-REQ-103 | Eligibility | Customer exists | Income below minimum criteria | Enter ₹8,000 salary | ₹8,000 | Validation displayed | High | Negative |
| ELG004 | LOS-REQ-104 | Eligibility | Customer exists | Age below minimum | DOB = 17 years | 17 Years | Application rejected | High | Boundary |
| ELG005 | LOS-REQ-105 | Eligibility | Customer exists | Age above maximum | DOB = 71 years | 71 Years | Validation displayed | High | Boundary |
| ELG006 | LOS-REQ-106 | Eligibility | Customer exists | Invalid PAN | Enter incorrect PAN | ABC123 | Validation displayed | Medium | Negative |
| ELG007 | LOS-REQ-107 | Eligibility | Customer exists | Invalid Aadhaar | Enter fewer than 12 digits | 123456 | Validation displayed | Medium | Negative |
| ELG008 | LOS-REQ-108 | Eligibility | Customer exists | Existing active loan | Select customer with active loan | Existing Loan | Business rule applied | High | Functional |
| ELG009 | LOS-REQ-109 | Eligibility | Customer exists | Monthly obligations exceed limit | EMI > Allowed DTI | Existing EMI | Customer not eligible | High | Functional |
| ELG010 | LOS-REQ-110 | Eligibility | Customer exists | Mobile number validation | Enter invalid mobile | 98765 | Validation displayed | Medium | Validation |
| ELG011 | LOS-REQ-111 | Eligibility | Customer exists | Email validation | Invalid email | abc@ | Validation displayed | Medium | Validation |
| ELG012 | LOS-REQ-112 | Eligibility | Customer exists | Customer nationality validation | Unsupported nationality | Test Data | Validation displayed | Low | Functional |
| ELG013 | LOS-REQ-113 | Eligibility | Customer exists | Employment type mandatory | Leave blank | NULL | Validation displayed | High | Mandatory |
| ELG014 | LOS-REQ-114 | Eligibility | Customer exists | Income proof mandatory | Skip upload | NULL | Validation displayed | High | Mandatory |
| ELG015 | LOS-REQ-115 | Eligibility | Customer exists | Eligible customer proceeds | Complete all validations | Valid Data | Continue to next stage | High | Positive |

---

# Business Rules

- Minimum age: 18 Years
- Maximum age: Configurable as per loan product
- Customer must complete KYC
- Income must satisfy loan product eligibility
- Mandatory documents should be uploaded
- Customer should not exceed Debt-to-Income (DTI) limits
- Customer must satisfy internal risk policies

---

# Exit Criteria

- Eligibility successfully evaluated.
- Validation messages displayed correctly.
- Eligible customer proceeds to the next workflow stage.
- Ineligible customer cannot continue.

---

# Test Summary

**Total Test Cases:** 15

**Positive:** 3

**Negative:** 6

**Boundary:** 2

**Validation:** 2

**Mandatory:** 2
