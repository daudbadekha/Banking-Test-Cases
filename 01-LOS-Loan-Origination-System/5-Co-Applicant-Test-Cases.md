# 🏦 Co-Applicant Management - Functional Test Cases

## Document Information

| Field | Value |
|-------|-------|
| Module | Loan Origination System (LOS) |
| Feature | Co-Applicant Management |
| Testing Type | Functional Testing |
| Version | 1.0 |
| Author | Daud Badekha |
| Last Updated | July 2026 |

---

# Objective

To verify that co-applicant details are captured, validated, modified, and linked correctly with the loan application.

---

# Preconditions

- Primary applicant exists.
- Loan application is created.
- User has permission to add co-applicants.
- Required KYC documents are available.

---

# Functional Test Cases

| TC ID | Requirement ID | Test Scenario | Test Steps | Test Data | Expected Result | Priority |
|------|----------------|---------------|------------|-----------|-----------------|----------|
| COAPP001 | LOS-CO-001 | Add co-applicant with valid details | Enter all mandatory information | Valid Data | Co-applicant added successfully | High |
| COAPP002 | LOS-CO-002 | Leave First Name blank | Skip First Name | Blank | Validation displayed | High |
| COAPP003 | LOS-CO-003 | Leave Last Name blank | Skip Last Name | Blank | Validation displayed | High |
| COAPP004 | LOS-CO-004 | Invalid Mobile Number | Enter 6 digits | 987654 | Validation displayed | Medium |
| COAPP005 | LOS-CO-005 | Invalid PAN | Enter incorrect PAN | ABC123 | Validation displayed | High |
| COAPP006 | LOS-CO-006 | Invalid Aadhaar | Enter 10 digits | 1234567890 | Validation displayed | High |
| COAPP007 | LOS-CO-007 | Duplicate PAN | Use existing PAN | Existing PAN | Duplicate validation | High |
| COAPP008 | LOS-CO-008 | Duplicate Aadhaar | Use existing Aadhaar | Existing Aadhaar | Duplicate validation | High |
| COAPP009 | LOS-CO-009 | Upload KYC documents | Upload Aadhaar & PAN | PDF | Upload successful | High |
| COAPP010 | LOS-CO-010 | Delete co-applicant | Remove co-applicant | Existing Record | Deleted successfully | Medium |
| COAPP011 | LOS-CO-011 | Modify co-applicant details | Update address | New Address | Updated successfully | Medium |
| COAPP012 | LOS-CO-012 | Verify relationship | Select Spouse | Spouse | Saved correctly | Medium |
| COAPP013 | LOS-CO-013 | Verify mandatory relationship | Leave blank | Blank | Validation displayed | Medium |
| COAPP014 | LOS-CO-014 | Verify age validation | Enter age below minimum | 17 Years | Validation displayed | High |
| COAPP015 | LOS-CO-015 | Save complete co-applicant | Complete all fields | Valid Data | Linked to loan application | High |
| COAPP016 | LOS-CO-016 | Reject invalid document | Upload expired PAN | Expired PDF | Validation displayed | Medium |
| COAPP017 | LOS-CO-017 | Verify audit trail | Save co-applicant | Valid Data | Audit log generated | Low |
| COAPP018 | LOS-CO-018 | View co-applicant profile | Open profile | Existing Data | Profile displayed | Low |
| COAPP019 | LOS-CO-019 | Add multiple co-applicants | Add second applicant | Valid Data | Added successfully | Medium |
| COAPP020 | LOS-CO-020 | Continue loan process | Complete all validations | Valid Data | Proceed to Credit Assessment | High |

---

# Business Rules

- Co-applicant PAN must be unique.
- Aadhaar validation is mandatory.
- Relationship with primary applicant is mandatory.
- Co-applicant KYC must be completed.
- Loan workflow cannot proceed with incomplete mandatory details.

---

# Exit Criteria

- Co-applicant linked successfully.
- Validation rules verified.
- Loan application updated.
- Audit logs generated.
