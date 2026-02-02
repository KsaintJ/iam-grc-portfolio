# Sample Evidence Index — IAM / GRC (Audit-Ready)

## Purpose
This index shows what evidence we collect, where it lives, and what it proves.

## Evidence map (SOC 2 / ISO 27001 style)
### Access requests & approvals
- **Evidence:** Ticket showing request + manager approval + implementation
- **Source:** Jira / Zendesk
- **Proves:** Access is authorized and tracked
- **Frequency:** Per request
- **Example file:** templates/examples/sample-quarterly-access-review-completed.md

### Joiner/Mover/Leaver (JML)
- **Evidence:** HR roster + provisioning ticket + deprovision confirmation
- **Source:** HR system + ticketing system + IAM logs
- **Proves:** Timely onboarding/offboarding and role changes
- **Frequency:** Per lifecycle event

### MFA enforcement
- **Evidence:** Screenshot/config export of MFA policy + sample auth logs
- **Source:** Okta / IdP
- **Proves:** Strong authentication for users (esp. privileged)
- **Frequency:** Quarterly + on change

### Privileged access reviews
- **Evidence:** Monthly admin list export + reviewer attestation + remediation tickets
- **Source:** IAM tool + ticketing
- **Proves:** Privileged access is controlled and reviewed
- **Frequency:** Monthly

### Logging & monitoring (IAM-relevant)
- **Evidence:** Auth logs, failed login alerts, admin actions log samples
- **Source:** SIEM / IAM / app logs
- **Proves:** Detection capability + traceability
- **Frequency:** Continuous; sample exported per audit

## Storage convention
- Evidence is referenced by ticket ID + date.
- Exports are stored in a secure location; repository contains sanitized examples only.

