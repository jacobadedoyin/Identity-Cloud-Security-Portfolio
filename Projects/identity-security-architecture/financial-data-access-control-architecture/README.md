# Financial Data Access Control Architecture

## Overview

This project presents a public-safe concept architecture for controlling access to sensitive financial data in a regulated cloud environment.

The design focuses on Microsoft Entra ID, MFA, Conditional Access, RBAC, least privilege, audit logging, and access governance. It demonstrates how identity controls can protect financial data platforms while supporting operational access needs.

![Financial Data Access Control Architecture](./images/architecture-diagram.png)

## Project Type

Concept architecture / portfolio design exercise.

This is a recreated model for portfolio evidence. It does not include live tenant configuration, real users, internal systems, client data, confidential architecture, or production screenshots.

## Architecture Focus

The architecture uses **Microsoft Entra ID** as the central identity and access control layer for financial data platforms.

It covers:

- Internal and external user access
- MFA and Conditional Access
- Group-based access assignment
- Role-Based Access Control
- Least privilege access
- Joiner, mover, and leaver access lifecycle
- Access reviews and governance
- Audit logging and monitoring

## Design Objectives

| Objective | Purpose |
|---|---|
| Centralised identity | Use Microsoft Entra ID as the main identity control point |
| Strong authentication | Require MFA for sensitive financial data access |
| Conditional Access | Control access using user, device, location, and risk signals |
| RBAC | Assign access through roles and groups instead of direct permissions |
| Least privilege | Limit users to the access required for their role |
| JML control | Support access changes when users join, move, or leave |
| Auditability | Log access activity for investigation and evidence |
| Access reviews | Regularly validate who still needs access |

## Access Flow

```text
User signs in
        ↓
Microsoft Entra ID verifies identity
        ↓
Conditional Access checks the request
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
