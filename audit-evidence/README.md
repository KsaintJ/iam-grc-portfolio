# Audit Evidence Example (IAM / GRC)

This document provides a sample of how IAM-related audit evidence would be prepared, organized, and presented during an internal or external audit (e.g., SOC 2, ISO 27001).

> All examples are generic and for demonstration purposes only.

---

## Scenario
Quarterly access review and identity lifecycle controls audit for in-scope applications.

---

## Evidence Types Collected

### 1. Access Reviews
- User access export per system
- Reviewer approval (manager/system owner)
- Evidence of access removals or modifications
- Completion attestation

**Supporting Artifacts**
- RBAC role–permission matrix
- Quarterly access review checklist
- Remediation tickets

---

### 2. Joiner–Mover–Leaver (JML)
- Joiner provisioning tickets with approval
- Mover role change documentation
- Leaver deprovisioning confirmation within SLA
- Logs/screenshots showing access removal

**Supporting Artifacts**
- JML evidence checklist
- Ticket IDs
- System logs

---

### 3. SSO / MFA Enforcement
- MFA policy configuration evidence
- Authentication logs (success/failure)
- Break-glass account documentation
- Exception approvals (if applicable)

**Supporting Artifacts**
- SSO/MFA rollout runbook
- Security configuration screenshots
- Log exports

---

## Evidence Retention
- Stored in centralized, access-controlled repository
- Retention aligned with audit and compliance requirements
- Access restricted to IAM, Security, and Audit teams

---

## Audit Readiness Outcome
- Clear traceability from control → execution → evidence
- Demonstrates least privilege, timely deprovisioning, and strong authentication controls
