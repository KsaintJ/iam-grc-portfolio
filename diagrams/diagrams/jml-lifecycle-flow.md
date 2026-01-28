# Joiner–Mover–Leaver (JML) Lifecycle Flow

## Overview
This diagram outlines how identity lifecycle events are handled from request through access changes and audit evidence retention.

---

## Joiner (New Hire)

HR System
→ Access Request Created
→ Manager Approval
→ IAM Provisioning (RBAC-based)
→ SSO/MFA Enrollment
→ Access Logged
→ Evidence Retained

---

## Mover (Role Change)

HR / Manager Request
→ Approval (Manager + System Owner)
→ Old Access Reviewed & Removed
→ New Role Access Provisioned
→ Logs Captured
→ Evidence Updated

---

## Leaver (Termination)

HR Termination Notice
→ Immediate Deprovisioning
→ Privileged Access Removed First
→ Sessions/Tokens Revoked
→ Confirmation Logged
→ Evidence Retained

---

## Audit Mapping
- Requests → Tickets
- Approvals → Attestations
- Changes → IAM logs
- Completion → Audit evidence repository
