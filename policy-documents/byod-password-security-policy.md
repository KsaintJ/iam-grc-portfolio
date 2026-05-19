# BYOD & Password Security Policy
## Professional Services Organization — Policy Brief

**Framework:** NIST Cybersecurity Framework (CSF) 2.0  
**Applicable Regulations:** Florida Bar Rule 1.6(c) · FIPA · HIPAA Security Rule · NIST SP 800-63B  
**Review Cadence:** Annual or upon material security incident  
**Author:** Kender Saint-Juste | GRC Portfolio Artifact

---

## I. Purpose

This policy establishes governance standards for Bring Your Own Device (BYOD) use and password security practices at a professional services organization handling privileged client communications, personally identifiable information (PII), and confidential case materials.

The mission: minimize unauthorized access, data loss, and regulatory non-compliance resulting from insecure personal device use and weak authentication practices — mapped to NIST CSF 2.0 controls proportionate to the organization's risk environment.

---

## II. Scope

Applies to all employees, contractors, and third parties accessing organizational systems, data, or client information — whether on organization-owned or personally owned devices. Covers all endpoints, accounts, and communication channels used for business purposes.

---

## III. Identified Vulnerabilities & Risk Assessment

| # | Vulnerability | Risk Description | Likelihood | Impact | NIST CSF Function |
|---|---|---|---|---|---|
| V-01 | Unmanaged Personal Devices | Personal devices access systems with no MDM, no encryption enforcement, no remote wipe. Lost/stolen device = immediate breach scenario. | High | High | PROTECT (PR.AA-3) |
| V-02 | Weak & Shared Password Practices | Shared credentials, written passwords, no complexity requirements or expiration enforcement. | High | High | PROTECT (PR.AA-1, PR.AA-7) |
| V-03 | No MFA on Remote Access | Remote authentication via single factor only. No secondary verification for client portals or email. | Medium | High | PROTECT (PR.AA-7) |
| V-04 | Inactive & Over-Privileged Accounts | Former users retain active accounts. Current staff hold excess permissions beyond job function. Violates least privilege. | Medium | High | IDENTIFY (ID.AM-6), PROTECT (PR.AA-4) |

**Overall Risk Rating:** HIGH — immediate governance controls required.

---

## IV. Controls (NIST CSF 2.0 Mapped)

### Control 1 — Formal BYOD Acceptable Use Policy
**Addresses:** V-01 | **NIST CSF:** GOVERN (GV.PO-1), PROTECT (PR.AA-3)

**Requirements:**
- All employees acknowledge BYOD policy in writing at onboarding and annually
- Permitted device types defined; minimum security configurations required before access (minimum OS version, screen lock, storage encryption)
- Client files must not be stored locally on personal devices; access via session-based authentication only
- MDM solution (e.g., Microsoft Intune, Jamf Now) required for any personal device accessing email, case management, or client portals
- MDM must enable remote wipe capability

**Evidence to Retain:** Signed acknowledgment forms · MDM enrollment logs · Device compliance reports

---

### Control 2 — Password Complexity, Rotation & Uniqueness
**Addresses:** V-02 | **NIST CSF:** PROTECT (PR.AA-1, PR.AA-7)

**Requirements (aligned to NIST SP 800-63B):**
- Minimum 12-character passwords; no dictionary words, personal names, or keyboard patterns
- Unique credentials per system; no shared accounts
- Rotation every 90 days for systems accessing client data
- Immediate reset upon known or suspected compromise
- Password manager provisioned for all staff (e.g., 1Password Teams, Bitwarden Business)
- Password manager access itself protected by MFA

**Evidence to Retain:** Policy acknowledgment signatures · Password manager enrollment logs · Rotation audit exports

---

### Control 3 — MFA for All Remote Access
**Addresses:** V-03 | **NIST CSF:** PROTECT (PR.AA-7)

**Requirements:**
- MFA mandatory on all remotely accessible systems: email, case management platform, client portals, cloud storage
- Minimum two factors: something known (password) + something possessed (authenticator app)
- SMS OTP discouraged; authenticator app preferred
- Existing staff: MFA enrollment within 30 days of policy adoption
- New hires: MFA enrollment before system access credentials issued

**Evidence to Retain:** MFA enforcement policy screenshots · Enrollment completion logs · Authentication event logs

---

### Control 4 — Account Lifecycle Management & Least Privilege
**Addresses:** V-04 | **NIST CSF:** IDENTIFY (ID.AM-6), PROTECT (PR.AA-4)

**Requirements:**
- All system access revoked within **24 hours** of employee/contractor separation
- Access inventory log maintained: every account, owner, access scope, last-reviewed date
- Log reviewed quarterly
- RBAC configured: users receive only permissions required for defined job function
- Role-based permissions reviewed semi-annually by authorized manager or system owner
- Privileged/admin accounts reviewed monthly

**Evidence to Retain:** Offboarding ticket with access revocation confirmation · Quarterly access review attestations · RBAC matrix with review dates · Exception log (with approvals and expiration)

---

## V. Regulatory Compliance Mapping

| Regulation / Standard | Governing Body | Relevance |
|---|---|---|
| Florida Bar Rule 1.6(c) | The Florida Bar | Requires reasonable efforts to prevent unauthorized disclosure of client information. Failure to implement security controls may constitute a professional conduct violation. |
| Florida Information Protection Act (FIPA) | State of Florida | Requires reasonable security measures for personal information; breach notification within 30 days of discovery. |
| NIST CSF 2.0 | NIST (U.S. Dept. of Commerce) | Primary governance framework. Controls map to GOVERN, IDENTIFY, and PROTECT functions. |
| NIST SP 800-63B | NIST | Password length, complexity, and storage standards. Password controls in Control 2 derived from Level of Assurance 2 requirements. |
| HIPAA Security Rule (45 CFR Part 164) | HHS | Applicable when handling protected health information (PHI) in matters involving medical records. Requires safeguards for PHI on any device. |

---

## VI. Roles & Responsibilities

| Role | Responsibilities |
|---|---|
| Executive / Managing Authority | Approves and enforces policy firm-wide. Conducts semi-annual access privilege reviews. Final authority on policy exceptions. |
| Operations Manager | Maintains account inventory log. Initiates deprovisioning within 24 hours of separation. Coordinates annual acknowledgment signatures. |
| IT Administrator / Contractor | Configures MDM, password manager, MFA enrollment. Executes remote wipe requests. Conducts quarterly access log reviews. Responds to security incidents within 4 business hours. |
| All Staff & Contractors | Enroll in MDM before accessing systems on personal devices. Use assigned password manager for all credentials. Complete MFA enrollment within 30 days. Report lost/stolen devices within 2 hours. Sign annual policy acknowledgment. |

---

## VII. Enforcement

Non-compliance results in progressive disciplinary action:
- **First violation:** Mandatory remediation training + documented written warning
- **Repeated violations / willful disregard:** Suspension of system access + potential termination
- **Violations involving client data disclosure:** Referred to legal counsel for professional conduct and liability assessment

---

## VIII. Definitions

| Term | Definition |
|---|---|
| BYOD | Bring Your Own Device — use of personally owned devices to access employer systems |
| MDM | Mobile Device Management — centralized software for device security configuration and remote management |
| MFA | Multi-Factor Authentication — two or more independent verification factors required before granting access |
| Least Privilege | Users, systems, and processes granted only minimum access rights necessary for their defined function |
| RBAC | Role-Based Access Control — permissions assigned to roles rather than individuals |
| PII | Personally Identifiable Information — data that can identify a specific individual |
| PHI | Protected Health Information — health data protected under HIPAA |

---

## IX. Evidence Summary for Audit

| Control | Evidence Type | Retention | Maps to SOC 2 |
|---|---|---|---|
| BYOD AUP | Signed acknowledgment forms + MDM enrollment logs | Duration of employment + 3 years | CC6.1, CC6.7 |
| Password Policy | Policy acknowledgment + rotation audit exports | Annual cycle + 3 years | CC6.1, CC6.2 |
| MFA Enforcement | Configuration screenshots + enrollment completion + auth logs | Ongoing + quarterly exports | CC6.1, CC6.2 |
| Account Lifecycle | Offboarding tickets + quarterly access review attestations | Duration of employment + 3 years | CC6.2, CC6.3 |

---

*Artifact: policy-documents/byod-password-security-policy.md*  
*Portfolio: github.com/KsaintJ/iam-grc-portfolio*  
*Framework: NIST CSF 2.0 | Regulations: Florida Bar Rule 1.6(c), FIPA, HIPAA, NIST SP 800-63B*
