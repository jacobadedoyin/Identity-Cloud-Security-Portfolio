# Financial Services Access Governance Architecture

<p>
  <strong><a href="../README.md">← Back to Identity Security Architecture</a></strong>
</p>

## Overview

This project presents a public-safe concept architecture for controlling access to sensitive financial data in a regulated cloud environment.

The design uses Microsoft Entra ID as the central identity layer, with MFA, Conditional Access, RBAC, least privilege, access reviews, and audit logging supporting secure access governance.

![Financial Data Access Control Architecture](./images/architecture-diagram.png)

---

## Architecture Focus

- Centralised identity control with Microsoft Entra ID
- MFA and Conditional Access for sensitive access
- Group-based RBAC instead of direct permissions
- Least-privilege access for financial data platforms
- Joiner, mover, and leaver access lifecycle controls
- Access reviews, audit logging, and monitoring

---

## Access Flow

```text
User signs in
        ↓
Microsoft Entra ID verifies identity
        ↓
Conditional Access evaluates the request
        ↓
MFA is required where needed
        ↓
Group membership is checked
        ↓
RBAC role defines access level
        ↓
Access is granted or denied
        ↓
Activity is logged for audit and review
