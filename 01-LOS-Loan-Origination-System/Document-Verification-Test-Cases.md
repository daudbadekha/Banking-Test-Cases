# 🏦 Document Verification - Functional Test Cases

## Document Information

| Field | Value |
|-------|-------|
| Module | Loan Origination System (LOS) |
| Feature | Document Verification |
| Testing Type | Functional Testing |
| Version | 1.0 |
| Author | Daud Badekha |
| Last Updated | July 2026 |

---

# Objective

To verify that all mandatory customer documents are uploaded, validated, and approved before the loan application proceeds to the next stage.

---

# Preconditions

- Customer profile exists.
- Loan application is created.
- KYC is completed.
- User has document verification access.
- Document checklist is configured.

---

# Functional Test Cases

| TC ID | Requirement ID | Test Scenario | Test Steps | Test Data | Expected Result | Priority |
|------|----------------|---------------|------------|-----------|-----------------|----------|
| DOC001 | LOS-DOC-001 | Upload Aadhaar Card | Upload valid Aadhaar PDF | Aadhaar.pdf | Upload successful | High |
| DOC002 | LOS-DOC-002 | Upload PAN Card | Upload PAN PDF | PAN.pdf | Upload successful | High |
| DOC003 | LOS-DOC-003 | Upload Salary Slip | Upload salary slip | SalarySlip.pdf | Upload successful | High |
| DOC004 | LOS-DOC-004 | Upload Bank Statement | Upload statement | Statement.pdf | Upload successful | High |
| DOC005 | LOS-DOC-005 | Upload Address Proof | Upload utility bill | AddressProof.pdf | Upload successful | High |
| DOC006 | LOS-DOC-006 | Skip mandatory document | Do not upload PAN | Blank | Validation displayed | High |
| DOC007 | LOS-DOC-007 | Upload unsupported file format | Upload .exe file | Test.exe | Validation displayed | High |
| DOC008 | LOS-DOC-008 | Upload oversized document | Upload 20MB file | Large.pdf | Validation displayed | Medium |
| DOC009 | LOS-DOC-009 | Upload corrupted PDF | Upload damaged file | Corrupt.pdf | Error displayed | Medium |
| DOC010 | LOS-DOC-010 | Upload duplicate document | Upload Aadhaar twice | Aadhaar.pdf | Duplicate prevented | Medium |
| DOC011 | LOS-DOC-011 | Delete uploaded document | Delete PAN | PAN.pdf | Document removed | Medium |
| DOC012 | LOS-DOC-012 | Re-upload corrected document | Upload corrected PAN | PAN_New.pdf | Upload successful | Medium |
| DOC013 | LOS-DOC-013 | Verify document preview | Click Preview | Uploaded file | Preview opens | Low |
| DOC014 | LOS-DOC-014 | Verify document download | Click Download | Uploaded file | Download successful | Low |
| DOC015 | LOS-DOC-015 | Verify mandatory checklist | Upload all required docs | Complete set | Checklist completed | High |
| DOC016 | LOS-DOC-016 | Approve document | Click Approve | Uploaded document | Status = Approved | High |
| DOC017 | LOS-DOC-017 | Reject document | Click Reject | Invalid document | Status = Rejected | High |
| DOC018 | LOS-DOC-018 | Reject without remarks | Reject document | Blank remarks | Validation displayed | Medium |
| DOC019 | LOS-DOC-019 | Verify audit log | Approve document | Valid file | Audit record created | Medium |
| DOC020 | LOS-DOC-020 | Continue after all approvals | Click Next | All approved | Move to Credit Assessment | High |

---

# Business Rules

- All mandatory documents must be uploaded.
- Only PDF, JPG and PNG formats are accepted.
- Maximum file size is configurable.
- Rejected documents must include remarks.
- Loan processing cannot continue until all mandatory documents are approved.

---

# Exit Criteria

- Mandatory documents uploaded.
- Document verification completed.
- Approval status updated.
- Workflow proceeds to Credit Assessment.
