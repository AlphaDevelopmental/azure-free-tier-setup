# Azure Free Tier Account Setup — Summary Report

**Author:** Taiwo Ajani  
**Date:** June 2026  
**Project:** Azure Free Tier Account Setup Complete Learning Program  
**Institution:** SQI College of ICT

---

## 1. Overview

This report documents the successful setup of a Microsoft Azure Free Tier environment as part of a foundational cloud computing learning program. The objective was to transition from theoretical cloud knowledge to hands-on practice by provisioning real cloud resources, exploring governance tools, and understanding security frameworks within the Azure platform.

---

## 2. Environment Summary

| Item | Detail |
|---|---|
| **Azure Account** | atmichealt94@gmail.com |
| **Subscription** | Azure subscription 1 |
| **Subscription Type** | Microsoft Azure Free Trial |
| **Available Credits** | $200.00 USD (expires July 8, 2026) |
| **Tenant / Directory** | Default Directory |
| **Resource Group Created** | `taiwo-cloud-lab-rg` |
| **Resource Deployed** | `taiwocloudlab001` (Storage Account) |
| **Deployment Region** | East US |

---

## 3. Region Selection Justification

### Chosen Region: East US (Virginia, USA)

The **East US** region was selected for this lab environment for the following reasons:

- **Broad Free Tier Availability:** East US is one of the most comprehensive Azure regions in terms of free-tier eligible services, ensuring maximum access to services within the $200 credit limit.
- **Service Maturity:** As one of Microsoft's oldest and most stable regions, East US offers the widest range of available services, making it ideal for learning and experimentation.
- **Reliability:** East US has multiple Availability Zones, providing physical redundancy across separate datacenters within the same region.

### Closest Geographic Region to Nigeria

While East US was selected for lab purposes, the geographically closest Azure region to Nigeria is:

- **South Africa North (Johannesburg)** — approximately 80ms average latency from Ibadan, Nigeria.
- **UAE North (Dubai)** — approximately 130ms average latency, suitable as a secondary option.

For a production deployment serving Nigerian users, **South Africa North** would be the recommended region to minimize latency and comply with data residency considerations.

---

## 4. Resource Deployed: Azure Storage Account

**Resource Name:** `taiwocloudlab001`  
**Resource Type:** Microsoft Azure Storage Account (PaaS)  
**Redundancy:** Locally Redundant Storage (LRS)  
**Performance Tier:** Standard  
**Region:** East US  
**Resource Group:** `taiwo-cloud-lab-rg`

### Why a Storage Account?

A Storage Account was chosen as the test deployment resource because:
- It falls within the Azure Free Tier limits (5 GB of locally redundant storage free for 12 months)
- It demonstrates the full Azure resource deployment workflow (configuration, review, validation, and provisioning)
- It carries no risk of unexpected charges under normal free-tier usage
- It illustrates both IaaS and PaaS concepts within a single service

---

## 5. Shared Responsibility Model

The **Shared Responsibility Model** defines the division of security obligations between Microsoft (the cloud provider) and the customer (the user). The boundaries shift depending on the service model used.

### How It Applies to the Storage Account Deployed

| Security Responsibility | Microsoft | Customer (Taiwo Ajani) |
|---|---|---|
| Physical datacenter security | ✅ | — |
| Network infrastructure & hardware | ✅ | — |
| Hypervisor and host OS | ✅ | — |
| Storage service availability & uptime | ✅ | — |
| Encryption at rest (default) | ✅ | — |
| Data classification and sensitivity | — | ✅ |
| Access control (IAM / RBAC) | — | ✅ |
| Secure transfer enforcement | — | ✅ (enabled) |
| Blob anonymous access policy | — | ✅ (disabled) |
| Monitoring and alerting configuration | — | ✅ |
| Cost management and budget limits | — | ✅ |

### Key Takeaway

Microsoft is responsible for securing the **infrastructure** the storage runs on. The customer is responsible for **what is stored**, **who can access it**, and **how it is configured**. In this deployment, secure defaults were maintained:

- **Secure transfer:** Enabled (forces HTTPS)
- **Blob anonymous access:** Disabled (no public read access)
- **Minimum TLS version:** 1.2 (modern encryption standard)
- **Redundancy:** LRS (3 copies within one datacenter)

---

## 6. Tasks Completed

| Task | Description | Status |
|---|---|---|
| 1 | Account Registration & Identity Verification | ✅ Complete |
| 2 | Azure Portal Exploration | ✅ Complete |
| 3 | Governance Setup — Subscription & Resource Group | ✅ Complete |
| 4 | Identity Awareness — Entra ID & RBAC | ✅ Complete |
| 5 | Region Selection & Availability Zone Research | ✅ Complete |
| 6 | Resource Deployment — Storage Account | ✅ Complete |
| 7 | Cost Management Configuration | ✅ Complete |

---

## 7. Key Learnings

- The Azure Portal provides a unified interface for managing all cloud resources across compute, storage, networking, and security domains.
- **Resource Groups** act as logical containers that simplify resource lifecycle management — deploying, monitoring, and deleting related resources together.
- **RBAC (Role-Based Access Control)** enables fine-grained access management, ensuring the principle of least privilege is applied across the environment.
- The **Shared Responsibility Model** makes clear that cloud security is a partnership — Microsoft secures the platform, but the customer must secure their data and configurations.
- **Cost Management tools** in Azure allow proactive monitoring of spend, helping learners and organizations stay within budget constraints.

---

## 8. Repository Structure

```
azure-free-tier-setup/
├── README.md
├── azure-setup-summary-report.md
├── screenshots/
│   ├── task1-portal-dashboard.png
│   ├── task3-resource-group.png
│   ├── task4-rbac.png
│   ├── task6-deployment-complete.png
│   ├── task6-storage-overview.png
│   └── task7-cost-analysis.png
```

---

*Report prepared as part of the Azure Free Tier Account Setup Complete Learning Program.*  
*Cloud Platform: Microsoft Azure | Learning Track: Cloud Computing Fundamentals*

---

## 9. Free Tier Resource Quotas

| Service | Free Tier Limit | Duration |
|---|---|---|
| Storage Account (LRS) | 5 GB | 12 months |
| Virtual Machines (B1s) | 750 hours/month | 12 months |
| Azure Functions | 1 million requests | Always free |
| Azure SQL Database | 250 GB | 12 months |
| Bandwidth (outbound) | 15 GB | Always free |
| Azure Active Directory | 50,000 objects | Always free |

## 10. Troubleshooting Notes

| Issue Encountered | Resolution |
|---|---|
| MFA enforcement page blocked portal access | Navigated directly to portal.azure.com/#home |
| GitHub HTTPS prompting for credentials repeatedly | Used `git config --global credential.helper store` |
| Card verification during signup | Used virtual dollar card with minimum $1 balance |
| Azure region not defaulting to Africa | Manually selected East US for broader free-tier support |
