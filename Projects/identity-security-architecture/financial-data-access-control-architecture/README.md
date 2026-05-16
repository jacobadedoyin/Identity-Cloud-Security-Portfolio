# Financial Services Access Governance Architecture

<p>
  <strong><a href="../README.md">← Back to Identity Security Architecture</a></strong>
</p>

## Overview

This project presents a public-safe access governance architecture for sensitive financial services data.

Financial platforms require stronger access control because permissions affect confidentiality, auditability, segregation of duties, reporting integrity, and trust in business-critical data. The design uses Microsoft Entra ID as the central identity layer, supported by MFA, Conditional Access, RBAC, least privilege, access reviews, and audit logging.

<p align="center">
  <img src="../../../assets/identity-security-architecture/financial-services-access-governance-architecture.png" alt="Financial Services Access Governance Architecture" width="900">
</p>

---

## Architecture Focus

- Microsoft Entra ID as the central identity control layer
- MFA and Conditional Access for sensitive access decisions
- Group-based RBAC aligned to business roles
- Least privilege and segregation of duties
- Joiner, mover, and leaver access lifecycle controls
- Access reviews, audit logging, and monitoring

---

## Access Flow

```text
User signs in
        ↓
Microsoft Entra ID verifies identity
        ↓
Conditional Access evaluates risk and context
        ↓
MFA is required where needed
        ↓
Group membership is checked
        ↓
RBAC role defines permitted access
        ↓
Access is granted or denied
        ↓
Activity is logged for audit and review
