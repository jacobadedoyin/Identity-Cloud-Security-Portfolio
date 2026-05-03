# Azure Administration and Operations

## Overview

This project area contains practical Azure administration and operational evidence.

The focus is on day-to-day Azure and Microsoft Entra administration tasks, operational reviews, access checks, monitoring, and evidence capture.

This area is intended for real workplace-aligned Azure work rather than certification notes only.

---

## Purpose

The purpose of this section is to evidence practical Azure administration capability across identity, access, monitoring, and operational control activities.

This may include:

- Emergency access / break-glass account review
- Conditional Access policy review
- Sign-in log review
- Inactive user review
- Privileged access review
- Azure Monitor and Log Analytics checks
- Operational worklogs
- Admin runbooks
- Evidence capture using sanitised screenshots, diagrams, and templates

---

## Areas Covered

| Area | Description |
| :--- | :--- |
| Identity administration | Microsoft Entra user, role, and access checks |
| Emergency access | Break-glass account review, configuration checks, and monitoring approach |
| Conditional Access | Reviewing policy coverage, exclusions, and access control impact |
| Sign-in review | Checking sign-in logs for unusual or important access activity |
| Privileged access | Reviewing elevated access, admin roles, and access justification |
| Inactive users | Identifying stale accounts or users requiring review |
| Monitoring | Using Azure Monitor, Log Analytics, alerts, and KQL where relevant |
| Operational evidence | Recording work safely through redacted or recreated evidence |

---

## Project Areas

| Project | Purpose | Status |
| :--- | :--- | :--- |
| **[Emergency Access Governance](./emergency-access-governance/)** | Evidence break-glass account review, exclusion checks, resilience considerations, and monitoring approach | In progress / documented |
| `conditional-access-review` | Document Conditional Access policy review and risk-based control checks | Planned |
| `inactive-user-review` | Evidence stale account identification and review process | Planned |
| `privileged-access-review` | Document privileged role review and least privilege checks | Planned |
| `sign-in-log-review` | Show how sign-in logs are reviewed for access and security assurance | Planned |
| `azure-monitoring-and-alerting` | Evidence Azure Monitor, Log Analytics, KQL, and alerting examples | Planned |
| `operational-worklog` | Track practical Azure administration tasks and outcomes | Planned |

---

## Current Evidence

The current active project in this section is:

```text
emergency-access-governance/
```

This project documents a workplace-aligned review of emergency access / break-glass account governance, including configuration review, identified control gaps, and recommended improvements.

---

## Evidence Approach

This section uses sanitised or recreated evidence only.

Suitable evidence includes:

- Redacted screenshots
- High-level diagrams
- Review templates
- Runbooks
- Worklog entries
- KQL examples
- PowerShell examples
- Configuration summaries using dummy data

Evidence must not include:

- Real user names
- Email addresses
- Tenant IDs
- Internal URLs
- Client information
- Ticket references
- Production secrets
- Real sign-in data
- Sensitive configuration details
- Confidential operational procedures

---

## Example Worklog Format

| Date | Area | Activity | Evidence |
| :--- | :--- | :--- | :--- |
| YYYY-MM-DD | Emergency Access | Reviewed break-glass account configuration and Conditional Access exclusions | Redacted screenshot / summary |
| YYYY-MM-DD | Conditional Access | Reviewed policy scope, exclusions, and admin impact | Policy register entry |
| YYYY-MM-DD | Sign-in Logs | Checked sign-in activity for emergency access account | Sanitised log summary |
| YYYY-MM-DD | Monitoring | Drafted alerting approach for rare privileged account usage | KQL example / diagram |

---

## Repository Structure

```text
azure-administration-and-operations/
├── README.md
└── emergency-access-governance/
    └── README.md
```

---

## Confidentiality Note

This section is designed to demonstrate Azure administration and operational capability without exposing confidential organisational information.

Any workplace-aligned evidence should be redacted, recreated, or summarised before being added to the portfolio.

---

## Summary

This section demonstrates practical Azure administration and Microsoft Entra ID operational capability.

It is focused on real-world aligned evidence such as emergency access review, Conditional Access considerations, sign-in monitoring, privileged access governance, and operational security documentation.
