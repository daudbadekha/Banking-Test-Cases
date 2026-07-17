# 🏦 Guarantor Management - Functional Test Cases

## Document Information

| Field | Value |
|-------|-------|
| Module | Loan Origination System (LOS) |
| Feature | Guarantor Management |
| Testing Type | Functional Testing |
| Version | 1.0 |
| Author | Daud Badekha |
| Last Updated | July 2026 |

---

# Objective

To verify that guarantor details are captured, validated, and linked correctly with the loan application before approval.

---

# Preconditions

- Primary applicant exists.
- Loan application is created.
- User has permission to add guarantors.
- Mandatory KYC documents are available.
- Loan product supports guarantors.

---

# Functional Test Cases

| TC ID | Requirement ID | Test Scenario | Test Steps | Test Data | Expected Result | Priority |
|------|----------------|---------------|------------|-----------|-----------------|----------|
| GUA001 | LOS-GUA-001 | Add guarantor with valid details | Enter mandatory information | Valid Data | Guarantor added successfully | High |
| GUA002 | LOS-GUA-002 | Leave First Name blank | Skip First Name | Blank | Validation message displayed | High |
| GUA003 | LOS-GUA-003 | Leave Mobile Number blank | Skip Mobile | Blank | Validation message displayed | High |
| GUA004 | LOS-GUA-004 | Invalid PAN Number | Enter invalid PAN | ABC123 | Validation displayed | High |
| GUA005 | LOS-GUA-005 | Invalid Aadhaar Number | Enter fewer than 12 digits | 1234567890 | Validation displayed | High |
| GUA006 | LOS-GUA-006 | Duplicate PAN | Enter existing PAN | Existing PAN | Duplicate validation displayed | High |
| GUA007 | LOS-GUA-007 | Duplicate Aadhaar | Enter existing Aadhaar | Existing Aadhaar | Duplicate validation displayed | High |
| GUA008 | LOS-GUA-008 | Upload KYC documents | Upload PAN & Aadhaar | PDF | Upload successful | High |
| GUA009 | LOS-GUA-009 | Upload unsupported file | Upload .exe | Test.exe | Validation displayed | Medium |
| GUA010 | LOS-GUA-010 | Upload oversized document | Upload 25MB PDF | Large.pdf | Validation displayed | Medium |
| GUA011 | LOS-GUA-011 | Edit guarantor details | Update address | New Address | Details updated | Medium |
| GUA012 | LOS-GUA-012 | Delete guarantor | Remove guarantor | Existing Record | Deleted successfully | Medium |
| GUA013 | LOS-GUA-013 | Verify guarantor age | Age below minimum | 17 Years | Validation displayed | High |
| GUA014 | LOS-GUA-014 | Verify guarantor income | Income below criteria | ₹5,000 | Validation displayed | High |
| GUA015 | LOS-GUA-015 | Verify employment details | Leave blank | NULL | Validation displayed | High |
| GUA016 | LOS-GUA-016 | Verify relationship | Select Friend | Friend | Saved successfully | Low |
| GUA017 | LOS-GUA-017 | Verify audit trail | Save guarantor | Valid Data | Audit record created | Low |
| GUA018 | LOS-GUA-018 | Add multiple guarantors | Add second guarantor | Valid Data | Saved successfully | Medium |
| GUA019 | LOS-GUA-019 | Submit application with guarantor | Complete mandatory details | Valid Data | Loan proceeds successfully | High |
| GUA020 | LOS-GUA-020 | Continue to Credit Assessment | Complete verification | Valid Data | Next workflow stage opened | High |

---

# Business Rules

- PAN must be unique.
- Aadhaar is mandatory.
- Guarantor KYC must be completed.
- Minimum age must satisfy configured policy.
- Loan cannot proceed if mandatory guarantor details are missing.

---

# Exit Criteria

- Guarantor linked successfully.
- Validation rules verified.
- Audit logs generated.
- Workflow proceeds to Credit Assessment.
