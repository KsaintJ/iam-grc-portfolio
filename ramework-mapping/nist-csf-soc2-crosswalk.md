# NIST CSF 2.0 → SOC 2 Trust Services Criteria Control Crosswalk

**Author:** Kender Saint-Juste  
**Framework Versions:** NIST Cybersecurity Framework 2.0 (2024) · AICPA SOC 2 Trust Services Criteria (2017, updated 2022)  
**Purpose:** Control mapping reference for compliance gap assessments, audit preparation, and GRC program alignment  
**Last Updated:** 2026

---

## How to Use This Crosswalk

This document maps NIST CSF 2.0 functions and categories to the corresponding SOC 2 Trust Services Criteria (TSC). Use it to:

- Identify which SOC 2 criteria are addressed by existing NIST CSF-aligned controls
- Spot coverage gaps where a SOC 2 criterion has no mapped NIST control
- Support dual-framework compliance programs (organizations pursuing both NIST alignment and SOC 2 Type II)
- Prepare evidence packages that satisfy both frameworks simultaneously

**Reading the table:** Each row maps one NIST CSF category to the SOC 2 TSC it most directly satisfies. Where one CSF category supports multiple TSC criteria, all are listed. Where a SOC 2 criterion has no direct NIST equivalent, it is flagged as a gap.

---

## Crosswalk Table

### GOVERN (GV) Function

| NIST CSF 2.0 Category | Category ID | SOC 2 TSC | TSC Description | Notes |
|---|---|---|---|---|
| Organizational Context | GV.OC | CC1.1, CC1.2 | Control Environment — Commitment to integrity, oversight structure | COSO Principle 1–2 alignment |
| Risk Management Strategy | GV.RM | CC3.1, CC3.2 | Risk Assessment — Specifies objectives, identifies risk | Foundational to SOC 2 risk assessment |
| Roles, Responsibilities, Authorities | GV.RR | CC1.3, CC1.4 | Control Environment — Accountability, reporting lines | Org chart and RACI documentation evidence |
| Policy | GV.PO | CC5.2, CC5.3 | Control Activities — Policies and procedures deployed | Policy acknowledgment records as evidence |
| Oversight | GV.OV | CC4.1, CC4.2 | Monitoring — Ongoing and separate evaluations | Board/management oversight documentation |
| Cybersecurity Supply Chain Risk Management | GV.SC | CC9.2 | Risk Mitigation — Vendor and business partner risk | Third-party risk management program |

---

### IDENTIFY (ID) Function

| NIST CSF 2.0 Category | Category ID | SOC 2 TSC | TSC Description | Notes |
|---|---|---|---|---|
| Asset Management | ID.AM | CC6.1, CC6.3 | Logical Access — Inventory of assets and authorized users | Asset inventory = prerequisite for access control |
| Risk Assessment | ID.RA | CC3.2, CC3.3, CC3.4 | Risk Assessment — Analyzes, develops response to risk | Risk register with likelihood × impact scoring |
| Improvement | ID.IM | CC4.1, CC4.2 | Monitoring — Evaluates and communicates deficiencies | Remediation tracking and closure evidence |

---

### PROTECT (PR) Function

| NIST CSF 2.0 Category | Category ID | SOC 2 TSC | TSC Description | Notes |
|---|---|---|---|---|
| Identity Management, Authentication, and Access Control | PR.AA | CC6.1, CC6.2, CC6.3 | Logical Access — Registration, authentication, removal of access | **Highest-density mapping.** RBAC, MFA, provisioning/deprovisioning all land here |
| Awareness and Training | PR.AT | CC1.4, CC2.2 | Control Environment / Communication — Competence, external communication | Security training records and acknowledgments |
| Data Security | PR.DS | CC6.6, CC6.7, A1.2 | Logical Access / Availability — Encryption, transmission protection, backup | Data classification and handling procedures |
| Platform Security | PR.PS | CC6.1, CC7.1 | Logical Access / System Operations — Configuration management, vulnerability detection | Hardening standards and baseline configurations |
| Technology Infrastructure Resilience | PR.IR | A1.1, A1.2, A1.3 | Availability — Capacity, backup, recovery | BCP/DR documentation |

---

### DETECT (DE) Function

| NIST CSF 2.0 Category | Category ID | SOC 2 TSC | TSC Description | Notes |
|---|---|---|---|---|
| Continuous Monitoring | DE.CM | CC7.1, CC7.2 | System Operations — Detects and monitors for anomalies | SIEM log evidence, alert configuration screenshots |
| Adverse Event Analysis | DE.AE | CC7.3, CC7.4 | System Operations — Evaluates and responds to anomalies | Incident triage documentation |

---

### RESPOND (RS) Function

| NIST CSF 2.0 Category | Category ID | SOC 2 TSC | TSC Description | Notes |
|---|---|---|---|---|
| Incident Management | RS.MA | CC7.3, CC7.4, CC7.5 | System Operations — Responds to identified anomalies and incidents | Incident response plan and post-mortem records |
| Incident Analysis | RS.AN | CC7.4 | System Operations — Analyzes identified anomalies | Root cause analysis documentation |
| Incident Response Reporting and Communication | RS.CO | CC2.3, CC7.5 | Communication / System Operations — Communicates relevant information | Breach notification records, escalation logs |
| Mitigation | RS.MI | CC7.5 | System Operations — Mitigates effects of detected events | Remediation tickets with closure evidence |

---

### RECOVER (RC) Function

| NIST CSF 2.0 Category | Category ID | SOC 2 TSC | TSC Description | Notes |
|---|---|---|---|---|
| Incident Recovery Plan Execution | RC.RP | A1.2, A1.3, CC7.5 | Availability / System Operations — Restores systems, communicates recovery | Recovery runbooks, RTO/RPO documentation |
| Incident Recovery Communication | RC.CO | CC2.3 | Communication — Communicates restoration activities | Stakeholder notification records |

---

## SOC 2 Coverage Gap Analysis

The following SOC 2 Trust Services Criteria have **limited or no direct NIST CSF equivalent** and require standalone controls or additional documentation:

| SOC 2 TSC | Description | Gap Notes |
|---|---|---|
| CC8.1 | Change Management — Changes to infrastructure, data, software | NIST CSF has no dedicated change management category. Requires separate change control policy and CAB records |
| CC9.1 | Risk Mitigation — Identifies and selects risk mitigation activities | Partially covered by GV.RM but SOC 2 requires explicit risk treatment decisions documented and reviewed |
| PI1.1–PI1.5 | Processing Integrity — Complete, valid, accurate, timely processing | NIST CSF does not address processing integrity. Relevant only for SaaS/data processing organizations |
| P1.1–P8.1 | Privacy Criteria | NIST Privacy Framework (separate from CSF) addresses this. Not covered in CSF 2.0 directly |
| A1.1 | Availability — Capacity planning | NIST CSF PR.IR partially covers this but SOC 2 requires explicit capacity threshold documentation |

---

## Evidence Mapping: What to Collect for Both Frameworks

For auditors reviewing both NIST CSF alignment and SOC 2 Type II, the following evidence satisfies multiple criteria simultaneously:

| Evidence Type | NIST CSF Categories Satisfied | SOC 2 TSC Satisfied |
|---|---|---|
| Access provisioning/deprovisioning tickets | PR.AA, ID.AM | CC6.1, CC6.2, CC6.3 |
| Quarterly access review attestations | PR.AA, GV.OV | CC6.3 |
| MFA enforcement configuration screenshots | PR.AA | CC6.1, CC6.2 |
| User access export reports | ID.AM, PR.AA | CC6.1, CC6.3 |
| Incident response records + post-mortems | RS.MA, RS.AN, RC.RP | CC7.3, CC7.4, CC7.5 |
| Security policy acknowledgment signatures | GV.PO, PR.AT | CC5.2, CC1.4 |
| Risk register with treatment decisions | GV.RM, ID.RA | CC3.1, CC3.2, CC3.3 |
| Vendor/third-party risk assessments | GV.SC | CC9.2 |
| Change management records | *(Gap — no direct NIST category)* | CC8.1 |

---

## Notes on Framework Versions

- This crosswalk uses **NIST CSF 2.0** (released February 2024), which added the **GOVERN** function not present in CSF 1.1. Organizations still aligned to CSF 1.1 should map the new GV categories to their existing controls or initiate a gap assessment.
- SOC 2 criteria reference the **2017 Trust Services Criteria** as updated. The criteria numbering (CC1.x through CC9.x, A1.x, PI1.x, P1.x–P8.x) is stable but organizations should verify against the current AICPA guidance.
- This crosswalk does not substitute for a formal audit or attestation. It is a practitioner reference tool.

---

## References

1. National Institute of Standards and Technology. (2024). *Cybersecurity Framework 2.0*. NIST. https://www.nist.gov/cyberframework
2. American Institute of Certified Public Accountants. (2017, updated 2022). *Trust Services Criteria for Security, Availability, Processing Integrity, Confidentiality, and Privacy (SOC 2)*. AICPA.
3. NIST. (2020). *NIST Special Publication 800-53 Rev 5: Security and Privacy Controls for Information Systems and Organizations*. https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final

---

*Artifact: framework-mapping/nist-csf-soc2-crosswalk.md*  
*Portfolio: github.com/KsaintJ/iam-grc-portfolio*
