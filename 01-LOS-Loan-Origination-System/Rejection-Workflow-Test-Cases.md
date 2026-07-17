# 🏦 Rejection Workflow - Functional Test Cases

## Document Information

| Field | Value |
|-------|-------|
| Module | Loan Origination System (LOS) |
| Feature | Rejection Workflow |
| Testing Type | Functional Testing |
| Version | 1.0 |
| Author | Daud Badekha |
| Last Updated | July 2026 |

---

# Objective

To verify that loan applications are rejected correctly based on business rules and that the rejection process is completely traceable.

---

# Preconditions

- Loan application exists.
- Credit Assessment completed.
- User has rejection authority.
- Approval workflow configured.

---

# Functional Test Cases

| TC ID | Requirement ID | Test Scenario | Test Steps | Test Data | Expected Result | Priority |
|------|----------------|---------------|------------|-----------|-----------------|----------|
| REJ001 | LOS-REJ-001 | Reject application | Click Reject | Valid Application | Status updated to Rejected | High |
| REJ002 | LOS-REJ-002 | Reject without remarks | Leave remarks blank | Blank | Validation displayed | High |
| REJ003 | LOS-REJ-003 | Reject with valid remarks | Enter rejection reason | Income criteria not met | Rejection successful | High |
| REJ004 | LOS-REJ-004 | Verify rejection timestamp | Reject application | Valid Data | Timestamp saved | Medium |
| REJ005 | LOS-REJ-005 | Verify rejected application search | Search Application ID | Rejected Loan | Record displayed | Medium |
| REJ006 | LOS-REJ-006 | Verify audit trail | Reject application | Valid Data | Audit record created | High |
| REJ007 | LOS-REJ-007 | Unauthorized rejection | Login without permission | Pending Loan | Access denied | High |
| REJ008 | LOS-REJ-008 | Reject already approved application | Open approved loan | Approved Loan | Rejection not allowed | High |
| REJ009 | LOS-REJ-009 | Reject already rejected application | Open rejected loan | Rejected Loan | Validation displayed | Medium |
| REJ010 | LOS-REJ-010 | Verify notification | Reject application | Valid Data | Notification generated | Medium |
| REJ011 | LOS-REJ-011 | Verify dashboard count | Reject application | Pending Loan | Count updated | Low |
| REJ012 | LOS-REJ-012 | Verify workflow history | View history | Rejected Loan | Rejection event displayed | Medium |
| REJ013 | LOS-REJ-013 | Verify application status | Open application | Rejected Loan | Status = Rejected | High |
| REJ014 | LOS-REJ-014 | Verify document retention | Reject application | Valid Data | Uploaded documents retained | Medium |
| REJ015 | LOS-REJ-015 | Verify loan cannot proceed | Attempt disbursement | Rejected Loan | Action blocked | High |
| REJ016 | LOS-REJ-016 | Verify application reopening (if allowed) | Click Reopen | Rejected Loan | Workflow follows business rule | Medium |
| REJ017 | LOS-REJ-017 | Verify rejection reason report | Generate report | Rejected Loans | Reason displayed | Low |
| REJ018 | LOS-REJ-018 | Verify rejection by approval level | Reject at Manager level | Valid Data | Workflow updated | Medium |
| REJ019 | LOS-REJ-019 | Verify remarks length | Enter maximum remarks | 500 Characters | Saved successfully | Low |
| REJ020 | LOS-REJ-020 | Verify end-to-end rejection process | Complete rejection workflow | Valid Data | Workflow completed successfully | High |

---

# Business Rules

- Rejection remarks are mandatory.
- Only authorized users can reject applications.
- Rejected applications cannot proceed to sanction or disbursement.
- Every rejection must be recorded in audit logs.
- Customer notification should be generated after rejection.

---

# Exit Criteria

- Application status updated to Rejected.
- Audit logs generated.
- Workflow history updated.
- Loan processing stopped.
