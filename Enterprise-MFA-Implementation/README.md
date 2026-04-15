# Enterprise MFA Implementation & Identity Governance

This project showcases the end-to-end technical implementation and governance framework for an enterprise-wide Multi-Factor Authentication (MFA) rollout within a global healthcare intelligence environment.

## ⚠️ Data Protection & Privacy Disclaimer
To maintain enterprise security and protect privileged healthcare data, all specific configuration files, internal server names, and sensitive instructions have been redacted. This documentation focuses on the **architectural methodology**, **governance standards**, and **engineering logic** applied during the implementation.

---

## 🎯 Project Overview
The objective was to transition a high-stakes clinical data environment from reactive access management to a proactive, identity-first security model.

* **Role:** Technical Implementation Lead
* **Focus:** Security Policy Configuration, Identity Lifecycle (JML), and SOP Standardisation.
* **Environment:** Hybrid Cloud (Azure Entra ID / SDA)

---

## 🛠️ Technical Implementation

### **Authentication & Security Policies**
* **Conditional Access:** Designed and implemented policies based on device compliance, geographical location (geofencing), and risk-based signals.
* **Protocol Management:** Configured secure authentication handshakes between the Identity Provider (IdP) and the SDA gateway.
* **RBAC Alignment:** Mapped user identities to specific cost centres and resource groups to ensure financial and security accountability.

### **Identity Lifecycle Integration (JML)**
I integrated the MFA enrolment process directly into the Joiner-Mover-Leaver (JML) lifecycle to ensure that security is enforced from Day 1 and revoked immediately upon exit.

```mermaid
graph LR
    A[HR Trigger] --> B[Entra ID Sync]
    B --> C[MFA Policy Applied]
    C --> D[Secure Access Granted]
