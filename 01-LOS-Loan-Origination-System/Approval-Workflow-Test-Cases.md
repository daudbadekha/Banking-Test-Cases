# 🏦 Approval Workflow - Functional Test Cases

## Document Information

| Field | Value |
|-------|-------|
| Module | Loan Origination System (LOS) |
| Feature | Approval Workflow |
| Testing Type | Functional Testing |
| Version | 1.0 |
| Author | Daud Badekha |
| Last Updated | July 2026 |

---

# Objective

To verify that loan applications are routed through the approval workflow according to business rules, authorization levels, and maker-checker controls.

---

# Preconditions

- Loan application submitted successfully.
- Credit Assessment completed.
- Customer passed eligibility checks.
- Required documents approved.
- Approver user account available.

---

# Workflow

Maker → Team Lead → Credit Manager → Branch Manager → Loan Approved

---

# Functional Test Cases

| TC ID | Requirement ID | Test Scenario | Test Steps | Test Data | Expected Result | Priority |
|------|----------------|---------------|------------|-----------|-----------------|----------|
| APR001 | LOS-APR-001 | Submit application for approval | Click Submit | Valid Application | Status changes to Pending Approval | High |
| APR002 | LOS-APR-002 | Approver views pending applications | Login as Approver | Pending Queue | Applications displayed | High |
| APR003 | LOS-APR-003 | Approve loan application | Click Approve | Eligible Loan | Status changes to Approved | High |
| APR004 | LOS-APR-004 | Reject loan application | Click Reject | Invalid Loan | Status changes to Rejected | High |
| APR005 | LOS-APR-005 | Reject without remarks | Leave remarks blank | Blank | Validation displayed | High |
| APR006 | LOS-APR-006 | Verify maker cannot approve own application | Login as Maker | Same Application | Approval restricted | High |
| APR007 | LOS-APR-007 | Verify checker approval | Login as Checker | Pending Loan | Approval successful | High |
| APR008 | LOS-APR-008 | Unauthorized user approval | Login without permission | Pending Loan | Access denied | High |
| APR009 | LOS-APR-009 | Verify approval history | Open History | Approved Loan | Approval trail displayed | Medium |
| APR010 | LOS-APR-010 | Verify approval timestamp | Approve loan | Valid Data | Timestamp recorded | Medium |
| APR011 | LOS-APR-011 | Verify approver remarks | Enter remarks | "Approved" | Remarks saved | Low |
| APR012 | LOS-APR-012 | Verify workflow notification | Approve loan | Valid Loan | Notification generated | Medium |
| APR013 | LOS-APR-013 | Verify multiple approval levels | Forward to next approver | Multi-level Workflow | Status updated | High |
| APR014 | LOS-APR-014 | Verify application lock during approval | Open by another user | Pending Loan | Record locked | Medium |
| APR015 | LOS-APR-015 | Verify audit log | Approve application | Valid Loan | Audit record created | High |
| APR016 | LOS-APR-016 | Verify approval dashboard count | Open Dashboard | Pending Loans | Count updated | Medium |
| APR017 | LOS-APR-017 | Verify approved application search | Search by Application ID | Approved Loan | Record found | Low |
| APR018 | LOS-APR-018 | Verify approval after document correction | Upload corrected document | Valid Loan | Approval allowed | Medium |
| APR019 | LOS-APR-019 | Verify application moves to disbursement | Final approval | Approved Loan | Status = Ready for Disbursement | High |
| APR020 | LOS-APR-020 | Verify end-to-end approval completion | Complete workflow | Valid Loan | Loan successfully approved | High |

---

# Business Rules

- Maker cannot approve their own application.
- Approval must follow configured hierarchy.
- Rejection requires mandatory remarks.
- Every approval action should be recorded in the audit log.
- Only authorized users can approve or reject applications.
- Fully approved loans should move to the disbursement stage.

---

# Exit Criteria

- Approval workflow completed successfully.
- Audit logs generated.
- Workflow status updated correctly.
- Approved applications available for loan disbursement.
