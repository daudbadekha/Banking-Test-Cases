# 🏦 Credit Assessment - Functional Test Cases

## Document Information

| Field | Value |
|-------|-------|
| Module | Loan Origination System (LOS) |
| Feature | Credit Assessment |
| Testing Type | Functional Testing |
| Version | 1.0 |
| Author | Daud Badekha |
| Last Updated | July 2026 |

---

# Objective

To verify that the system correctly evaluates the applicant's financial eligibility, repayment capacity, and credit profile before forwarding the loan for approval.

---

# Preconditions

- Loan application submitted.
- Customer Eligibility completed.
- KYC approved.
- Documents verified.
- Co-Applicant/Guarantor added (if applicable).

---

# Functional Test Cases

| TC ID | Requirement ID | Test Scenario | Test Steps | Test Data | Expected Result | Priority |
|------|----------------|---------------|------------|-----------|-----------------|----------|
| CA001 | LOS-CA-001 | Verify income calculation | Enter salary details | ₹75,000 | Income calculated correctly | High |
| CA002 | LOS-CA-002 | Verify self-employed income | Enter business income | ₹1,50,000 | Income accepted | High |
| CA003 | LOS-CA-003 | Income below minimum eligibility | Enter ₹8,000 | ₹8,000 | Application marked ineligible | High |
| CA004 | LOS-CA-004 | Verify Debt-to-Income Ratio | Existing EMI ₹30,000 | DTI calculated | High |
| CA005 | LOS-CA-005 | Existing loan validation | Add active loan | Existing loan | Display warning | High |
| CA006 | LOS-CA-006 | Verify maximum loan eligibility | Calculate eligible amount | Valid profile | Eligible amount displayed | High |
| CA007 | LOS-CA-007 | Verify minimum loan amount | Enter below minimum | ₹5,000 | Validation displayed | Medium |
| CA008 | LOS-CA-008 | Verify repayment capacity | Calculate EMI | 60 Months | Repayment calculated | High |
| CA009 | LOS-CA-009 | Invalid employment type | Select invalid value | Test | Validation displayed | Medium |
| CA010 | LOS-CA-010 | Missing income proof | Remove salary slip | Missing document | Assessment blocked | High |
| CA011 | LOS-CA-011 | Verify customer risk category | Assess profile | Standard | Risk displayed | Medium |
| CA012 | LOS-CA-012 | Verify multiple income sources | Salary + Rental | Mixed income | Total calculated | Medium |
| CA013 | LOS-CA-013 | Verify guarantor impact | Add guarantor | Valid guarantor | Eligibility recalculated | Medium |
| CA014 | LOS-CA-014 | Verify co-applicant income | Add co-applicant | Joint income | Loan eligibility updated | High |
| CA015 | LOS-CA-015 | Verify final assessment status | Complete assessment | Valid profile | Status = Eligible | High |
| CA016 | LOS-CA-016 | Reject assessment | Mark Not Eligible | Invalid profile | Status = Rejected | High |
| CA017 | LOS-CA-017 | Verify assessment remarks | Save remarks | Remarks | Stored successfully | Low |
| CA018 | LOS-CA-018 | Verify assessment history | Open history | Existing case | History displayed | Low |
| CA019 | LOS-CA-019 | Verify audit logs | Complete assessment | Valid data | Audit entry created | Medium |
| CA020 | LOS-CA-020 | Forward to Approval | Click Forward | Eligible case | Sent to Approval Workflow | High |

---

# Business Rules

- Customer must satisfy minimum income criteria.
- Existing liabilities should be considered.
- Debt-to-Income ratio must be within policy limits.
- Mandatory income proof is required.
- Assessment cannot proceed if mandatory validations fail.
- Only eligible applications proceed to approval.

---

# Exit Criteria

- Credit assessment completed successfully.
- Eligibility decision recorded.
- Assessment history updated.
- Application forwarded to Approval Workflow.
