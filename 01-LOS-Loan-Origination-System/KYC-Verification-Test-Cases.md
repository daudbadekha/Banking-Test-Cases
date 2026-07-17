# 🏦 KYC Verification - Functional Test Cases

## Document Information

| Field | Value |
|-------|-------|
| Module | Loan Origination System (LOS) |
| Feature | KYC Verification |
| Testing Type | Functional Testing |
| Version | 1.0 |
| Author | Daud Badekha |
| Last Updated | July 2026 |

---

# Objective

To validate the Know Your Customer (KYC) verification process before loan processing.

---

# Preconditions

- Customer profile exists.
- Loan application is created.
- User has KYC verification access.
- Required KYC document types are configured.

---

# Functional Test Cases

| TC ID | Requirement ID | Test Scenario | Test Steps | Test Data | Expected Result | Priority |
|------|----------------|---------------|------------|-----------|-----------------|----------|
| KYC001 | LOS-KYC-001 | Verify Aadhaar upload | Upload valid Aadhaar | Aadhaar PDF | Upload successful | High |
| KYC002 | LOS-KYC-002 | Verify PAN upload | Upload valid PAN | PAN PDF | Upload successful | High |
| KYC003 | LOS-KYC-003 | Upload unsupported file type | Upload EXE file | .exe | Validation displayed | High |
| KYC004 | LOS-KYC-004 | Upload oversized file | Upload 15 MB PDF | Large File | Validation displayed | Medium |
| KYC005 | LOS-KYC-005 | Mandatory Aadhaar validation | Skip Aadhaar | Blank | Validation displayed | High |
| KYC006 | LOS-KYC-006 | Mandatory PAN validation | Skip PAN | Blank | Validation displayed | High |
| KYC007 | LOS-KYC-007 | Invalid Aadhaar Number | Enter 10 digits | 1234567890 | Validation displayed | High |
| KYC008 | LOS-KYC-008 | Invalid PAN Format | Enter ABC123 | Invalid PAN | Validation displayed | High |
| KYC009 | LOS-KYC-009 | Expired ID Proof | Upload expired document | Expired PDF | Validation displayed | Medium |
| KYC010 | LOS-KYC-010 | Duplicate Document Upload | Upload same document twice | Aadhaar | Duplicate prevented | Medium |
| KYC011 | LOS-KYC-011 | Verify document preview | Click Preview | Uploaded File | Preview displayed | Low |
| KYC012 | LOS-KYC-012 | Delete uploaded document | Delete document | Uploaded File | Document removed | Low |
| KYC013 | LOS-KYC-013 | Re-upload corrected document | Upload new file | Updated PDF | Upload successful | Medium |
| KYC014 | LOS-KYC-014 | Verify KYC completion status | Complete all documents | Valid Docs | Status = Completed | High |
| KYC015 | LOS-KYC-015 | Submit loan without completed KYC | Click Submit | Missing KYC | Submission blocked | High |

---

# Business Rules

- Aadhaar is mandatory.
- PAN is mandatory.
- Only configured document types are accepted.
- File size must be within configured limits.
- Loan processing cannot continue until KYC is complete.

---

# Exit Criteria

- All mandatory documents uploaded.
- KYC status updated successfully.
- Validation messages verified.
- Loan workflow proceeds only after successful KYC.
