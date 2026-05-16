# 🛡️ Cybersecurity Operations and Governance

[← Back to Portfolio Overview](../README.md)

## Overview

This project demonstrates cybersecurity operations and governance activities focused on vulnerability management, patching support, security testing awareness, and remediation tracking.

The work uses a public-safe model based on Qualys-style vulnerability scanning, patch governance, prioritisation, evidence capture, and penetration testing support.

---

## Project Focus

| Area | Evidence Focus |
|---|---|
| Vulnerability management | Identifying, reviewing, prioritising, and tracking security weaknesses across systems |
| Qualys-style scanning | Understanding scan outputs, severity ratings, asset exposure, and remediation evidence |
| Patch governance | Supporting patching activity, ownership, follow-up, exception handling, and closure evidence |
| Remediation tracking | Recording findings, owners, actions, status, target dates, and completion evidence |
| Risk prioritisation | Assessing severity, exploitability, business impact, and exposure before remediation |
| Penetration testing support | Supporting test planning, evidence handling, findings review, and remediation follow-up |
| Governance reporting | Producing clear, public-safe summaries for risk review, audit, and operational assurance |

---

## Tools and Methods

| Tool / Method | Purpose |
|---|---|
| Qualys | Vulnerability scanning, asset visibility, severity review, and remediation evidence |
| Patch management process | Track patch activity, exceptions, ownership, and completion status |
| Risk register / tracker | Record vulnerability findings, business impact, remediation owner, and closure status |
| Penetration testing outputs | Review findings, confirm affected areas, and support remediation planning |
| Evidence pack | Maintain screenshots, templates, trackers, and public-safe governance documentation |

---

## Security Operations Workflow

```mermaid
flowchart LR
    A[Asset or system in scope] --> B[Qualys-style vulnerability scan]
    B --> C[Finding review and severity validation]
    C --> D[Risk prioritisation]
    D --> E[Patch or remediation owner assigned]
    E --> F[Remediation or exception tracked]
    F --> G[Validation and closure evidence]
    G --> H[Governance reporting]
