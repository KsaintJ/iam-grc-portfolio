# RBAC Provisioning Flow (Request → Approval → Provision → Evidence)

## Overview
This diagram shows a practical RBAC provisioning workflow designed to enforce least privilege, separation of duties (SoD), and audit-ready evidence collection.

---

## RBAC Provisioning Lifecycle

**User / Manager Request**  
→ Access request submitted (ticket / portal)  
→ Includes: system, role, justification, start/end date (if temporary), manager

**Policy & Role Mapping**  
→ IAM reviews request against:
- Role catalog / entitlement model
- SoD rules (conflict checks)
- Least privilege policy
- Joiner/Mover/Leaver alignment

**Approval Workflow**
→ Manager approval (business need)  
→ System Owner / App Owner approval (risk + access appropriateness)  
→ Security/IAM approval (policy + SoD + risk-based)

**Provisioning Execution**
→ IAM provisions access via:
- IGA platform / directory groups
- SSO assignments
- Application role assignment
→ MFA enforced for privileged / sensitive access

**Verification / Validation**
→ Confirm access granted correctly
- Correct role/entitlements
- Correct scope (prod vs non-prod)
- Correct duration (if time-bound)
→ Optional: user attestation (“I can access what I need”)

**Logging & Evidence Capture**
→ Evidence retained:
- Ticket ID + approvals
- Role assigned + timestamp
- Provisioning actor (system or admin)
- MFA enrollment proof (if applicable)
- SoD check result / exemption record

**Ongoing Governance**
→ Quarterly access review / recertification  
→ Triggered revalidation for:
- Role changes
- Privilege escalation
- High-risk systems

---

## Control Intent (Audit Language)
- **Least privilege:** access is role-based, scoped, and time-bound when appropriate  
- **SoD enforcement:** conflicts prevented or documented with approvals and exceptions  
- **Accountability:** approvals and provisioning actions are attributable  
- **Auditability:** evidence is captured and retained to support compliance reviews

