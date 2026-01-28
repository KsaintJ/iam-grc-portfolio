# IAM / GRC Portfolio
> This repository demonstrates how I design, document, and validate IAM controls the same way they are reviewed in real audits and security assessments.

Job-ready IAM/GRC portfolio demonstrating practical access governance,
identity lifecycle controls, and SSO/MFA implementation with audit-ready
documentation.

## Projects

### 1. Access Reviews & RBAC Framework
📁 `/access-reviews-rbac`  
- Role-based access control (RBAC)
- Quarterly access reviews
- Exception handling
- Audit evidence collection

### 2. Joiner–Mover–Leaver (JML) Lifecycle Controls
📁 `/jml-lifecycle-controls`  
- Identity lifecycle governance
- Provisioning, role changes, deprovisioning
- Approval workflows and SLAs
- Evidence retention for audits

### 3. SSO / MFA Rollout Runbook
📁 `/sso-mfa-runbook`  
- IdP integration (SAML / OAuth)
- MFA enforcement strategy
- Break-glass access handling
- Logging and audit readiness

## Framework Alignment
- SOC 2
- ISO 27001
- Least Privilege
- Audit Readiness

## Audit Evidence Example
A sample walkthrough of how IAM controls and supporting documentation would be presented during an audit.  
**Folder:** `audit-evidence/`

## Diagrams
High-level visuals illustrating IAM lifecycle and governance flows.  
**Folder:** `diagrams/`

## How I’d Walk an Auditor or Security Lead Through This (2–3 Minutes)

**1. Start with control objectives**
The goal of this IAM program is to ensure:
- Access is granted based on role and business need (least privilege)
- All access changes are approved, logged, and attributable
- Separation of duties is enforced or formally documented
- Evidence is retained to support audits and investigations

**2. Explain lifecycle-driven access**
I begin with Joiner–Mover–Leaver (JML) because identity lifecycle events
are the primary risk driver for unauthorized access.

- Joiners receive role-based access aligned to job function
- Movers trigger access review and re-provisioning
- Leavers are deprovisioned within defined SLAs

This ensures access stays aligned with employment status and role.

**3. Show how RBAC enforces consistency**
RBAC standardizes access by mapping roles to approved entitlements.
This reduces manual decisions, prevents privilege creep, and enables
repeatable approvals.

- Requests follow defined approval paths
- Roles are pre-approved and reviewed periodically
- Privileged access is restricted and monitored

**4. Explain secure access enforcement**
SSO and MFA are enforced to:
- Reduce credential sprawl
- Strengthen authentication for sensitive systems
- Provide centralized logging for access activity

Privileged or high-risk access requires MFA by design.

**5. Prove it with evidence**
For every control, there is supporting evidence:
- Tickets show requests and approvals
- Logs show provisioning actions and timestamps
- Access reviews show periodic recertification
- Exceptions are documented, approved, and time-bound

Evidence is organized to be audit-ready, not retroactively assembled.

**6. What I would test as an auditor**
- Can access be granted without approval? (should fail)
- Are terminated users removed within SLA?
- Are privileged roles protected by MFA?
- Are access reviews completed and documented on schedule?

