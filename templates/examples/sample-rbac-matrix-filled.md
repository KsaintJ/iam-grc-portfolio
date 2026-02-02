# Sample RBAC Role–Permission Matrix (Filled Example)

> Example org: “Acme Health Services” (mid-size SaaS + HIPAA-aligned workflows)

## Applications in scope
- Okta (IdP)
- Google Workspace
- Jira
- Zendesk
- AWS Console (limited admins)
- Patient Portal (internal admin panel)

## Roles
### Role: Support Agent (Tier 1)
**Business purpose:** Resolve customer issues without privileged system access.  
**Owner:** Support Manager  
**Review cadence:** Quarterly

| Application | Permission/Group | Access Level | Approved By | Notes |
|---|---|---:|---|---|
| Okta | group: support-tier1 | Standard | Support Mgr | Required for SSO app access |
| Zendesk | role: agent | Standard | Support Ops | Tickets + customer comms |
| Jira | project: SUPPORT browse/create | Standard | Support Ops | Bug/issue creation only |
| Google Workspace | support@ shared inbox | Standard | IT | No admin console access |
| Patient Portal | none | None | N/A | Explicitly denied |
| AWS Console | none | None | N/A | Explicitly denied |

### Role: Support Lead (Tier 2)
**Owner:** Support Director  
**Review cadence:** Quarterly

| Application | Permission/Group | Access Level | Approved By | Notes |
|---|---|---:|---|---|
| Zendesk | role: admin-lite | Elevated | Support Director | Can manage macros, views |
| Jira | project: SUPPORT admin | Elevated | Engineering Manager | Can triage + manage queues |
| Google Workspace | group: support-leads | Standard | IT | For lead-only resources |

### Role: IAM Admin (Privileged)
**Owner:** Security (GRC/IAM)  
**Review cadence:** Monthly

| Application | Permission/Group | Access Level | Approved By | Notes |
|---|---|---:|---|---|
| Okta | role: super admin (break-glass) | Privileged | CISO | Break-glass only; MFA enforced |
| Okta | role: app admin | Privileged | Security Manager | Daily IAM admin |
| AWS | IAMReadOnly | Elevated | Cloud Owner | Separate approval path |

## Least privilege notes
- Tier 1 cannot access Patient Portal admin or AWS.
- Privileged roles require MFA + logging + monthly review.

