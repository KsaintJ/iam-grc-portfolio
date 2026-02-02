# Sample Quarterly Access Review (Completed)

**System:** Zendesk  
**Review period:** Q4 2025 (Oct 1 – Dec 31, 2025)  
**Reviewer:** Support Operations Manager  
**Control intent:** Ensure user access is appropriate and least privilege is maintained.

## Evidence captured
- [x] User export (CSV) from Zendesk admin console
- [x] HR roster (active employees list)
- [x] Exceptions + approvals (ticket links)
- [x] Remediation tickets
- [x] Final attestation statement

## Findings
### 1) Dormant accounts identified
- **Finding:** 2 users inactive > 90 days
- **Action:** Disable accounts
- **Tickets:** IT-2211, IT-2212
- **Status:** Completed

### 2) Excess permissions
- **Finding:** 1 Tier 1 agent had “admin-lite”
- **Action:** Role reduced to “agent”
- **Approval:** Support Director approval recorded in IT-2215
- **Status:** Completed

### 3) Leaver access
- **Finding:** 1 terminated user still active (HR roster mismatch)
- **Action:** Disabled immediately; postmortem opened
- **Root cause:** Offboarding ticket not created
- **Preventive action:** Update JML checklist; add HR→IT trigger
- **Tickets:** IT-2220 (disable), GRC-104 (process fix)
- **Status:** Completed

## Attestation
I confirm I reviewed Zendesk access for the review period and verified access aligns with job responsibilities and least privilege.

**Signed:** Support Ops Manager  
**Date:** 2026-01-05

