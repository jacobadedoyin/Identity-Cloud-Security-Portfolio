# 🏦 Enterprise IAM Architecture for Financial Data Access & Governance
**Identity Lifecycle, Access Control, and Security Design for Regulated Environments**

---

## 📌 Overview

This project presents a practical Identity and Access Management (IAM) architecture designed to secure access to **sensitive financial data platforms** within a regulated environment.

The design reflects real-world IAM challenges, including:

- Managing internal and external identities  
- Securing access to data and analytics platforms  
- Enforcing strong authentication and access controls  
- Supporting auditability and regulatory compliance  

The solution is built around **Microsoft Entra ID**, focusing on **identity lifecycle management, RBAC design, and access governance**.

---

## 🎯 Objectives

- Design a secure IAM architecture for financial data access  
- Enforce strong authentication using Multi-Factor Authentication (MFA)  
- Implement role-based access control (RBAC) aligned to least privilege  
- Support identity lifecycle processes (Joiners, Movers, Leavers)  
- Enable access governance through reviews and auditing  
- Align with regulatory and data security requirements  

---

## 🏗️ Architecture Design

### Core Components

- **Identity Provider:** Microsoft Entra ID  
- **Authentication Layer:** MFA and Conditional Access  
- **Access Control Layer:** RBAC via security groups  
- **Applications:** Financial data platforms (reporting, analytics, BI tools)  
- **User Types:** Internal staff, external partners  

---

### 🔄 Access Flow

1. User authenticates via Microsoft Entra ID  
2. Conditional Access policies evaluate:
   - Location  
   - Device compliance  
   - Risk signals  
3. Multi-Factor Authentication is enforced  
4. Access is granted via group-based RBAC  
5. Activity is logged and monitored for audit  

---

## 🔐 Access Model Design

### Role-Based Access Control (RBAC)

Access is assigned through **security groups**, not directly to users.

#### Example Role Structure

| Role | Access Scope |
|------|-------------|
| Data Analyst | Read access to financial datasets |
| Finance Manager | Read/write access to reporting systems |
| Platform Admin | Full access to data platforms |
| External Partner | Restricted access to specific datasets |

---

### Key Principles

- **Least Privilege:** Users receive only the access required  
- **Separation of Duties:** Admin and user roles are segregated  
- **Scalability:** Access managed through group membership  
- **Consistency:** Standardised access assignment model  

---

## 🔄 Identity Lifecycle (JML)

### Joiners
- User accounts provisioned in Entra ID  
- Assigned to role-based groups  
- Access granted automatically via RBAC  

### Movers
- Role or department changes trigger group updates  
- Previous access removed  
- New access assigned based on role  

### Leavers
- Immediate account disablement  
- Removal from all access groups  
- Access revoked across all systems  

---

## 🔐 Authentication & Security Controls

### Multi-Factor Authentication (MFA)

- Enforced for all users accessing financial systems  
- Additional controls for privileged roles  

---

### Conditional Access (Conceptual Design)

- **Location-based restrictions:** Block access from high-risk regions  
- **Device compliance:** Require managed or compliant devices  
- **Risk-based policies:** Trigger additional verification when needed  

---

## 📊 Access Governance

### Access Reviews

- Periodic validation of user permissions  
- Removal of unnecessary or excessive access  
- Focus on privileged and external users  

---

### Auditing & Monitoring

- Logging of authentication and access events  
- Monitoring for abnormal or high-risk behaviour  
- Support for audit and compliance reporting  

---

## 🧪 Use Case Scenario

This architecture models a financial organisation where users require secure access to **data platforms used for reporting and analytics**.

The design ensures:

- Secure access for both internal and external users  
- Controlled exposure of financial data  
- Strong governance over permissions and identity lifecycle  

---

## 🧠 Key Design Principles

- **Security First:** Zero Trust-aligned approach  
- **Identity as Control Plane:** Access governed through identity  
- **Least Privilege:** Minimal access by default  
- **Auditability:** All access is traceable  
- **Scalability:** Designed for enterprise environments  

---

## 🔮 Future Enhancements

- Integration with **Privileged Identity Management (PIM)**  
- Automated provisioning workflows (approval-based access)  
- Advanced Conditional Access policies  
- Integration with enterprise access governance tools  

---

## 🎯 Outcome

This project demonstrates a structured IAM architecture that combines:

- Identity lifecycle management  
- Secure authentication controls  
- Role-based access design  
- Governance and compliance enforcement  

It reflects real-world IAM design considerations relevant to **financial services and regulated environments**.

---

*Maintained by Jacob Adedoyin*
