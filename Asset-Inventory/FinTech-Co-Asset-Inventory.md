# Information & Technology Asset Inventory

**Organisation:** FinTech Co (Fictional - 50 employees)  
**Document ID:** AST-001  
**Version:** 1.0  
**Effective Date:** March 2026  
**Last Reviewed:** November 2026  
**Owner:** IT Operations / CISO  
**Classification:** Internal  
**Framework Alignment:** ISO/IEC 27001 (A.8.1) | NIST CSF 2.0 (ID.AM-01, ID.AM-02, ID.AM-03, ID.AM-07) | PCI DSS v4.0 (Req. 2.4, 9.4)  

---

## 1. Overview & Purpose

Maintaining an accurate and up-to-date asset inventory is fundamental to information security, risk management, and regulatory compliance. This inventory documents all hardware, software, services, data repositories, and third-party systems deployed across FinTech Co.

In accordance with the **FinTech Co Information Security Policy (POL-001)** and **Data Classification Policy (POL-005)**, each asset is assigned:
- A designated business/technical owner accountable for its security.
- A critical business impact tier (**Tier 1 - Mission Critical**, **Tier 2 - Business Operational**, **Tier 3 - Standard / Administrative**).
- A data classification level (**Restricted**, **Confidential**, **Internal**, or **Public**).
- An overview of existing baseline controls and lifecycle status.

---

## 2. Asset Criticality & Classification Definitions

| Criticality Tier | Definition | RTO Target | RPO Target |
|---|---|:---:|:---:|
| **Tier 1 - Mission Critical** | Core payment services, primary database, and customer authentication systems whose failure causes immediate financial and regulatory harm. | < 4 hours | < 1 hour |
| **Tier 2 - Business Operational** | Supporting tools, CRM, build pipelines, and business databases essential for daily business conduct. | < 24 hours | < 12 hours |
| **Tier 3 - Standard / Admin** | Internal administrative tooling, knowledge repositories, and standard workstations. | < 72 hours | < 24 hours |

---

## 3. Hardware & Infrastructure Assets (ID.AM-01)

| Asset ID | Asset Name | Description & Specification | Primary Location / Environment | Assigned Owner | Criticality | Data Classification | Baseline Controls |
|---|---|---|---|---|:---:|:---:|---|
| **HW-001** | Production Cloud VPC | AWS Primary VPC (us-east-1) hosting containerised APIs and web services | Cloud (AWS) | Cloud Architect | Tier 1 | Restricted | Multi-AZ, IaC, Network ACLs, GuardDuty, AWS WAF |
| **HW-002** | Disaster Recovery VPC | AWS Secondary VPC (us-west-2) for warm standby disaster recovery | Cloud (AWS) | Cloud Architect | Tier 1 | Restricted | Automated database read replicas, cross-region backups |
| **HW-003** | Corporate Laptops (Fleet) | 55x Apple MacBook Pro / Dell XPS issued to staff and contractors | Remote / Office | IT Operations | Tier 2 | Confidential | FileVault/BitLocker full-disk encryption, MDM enrolled, EDR |
| **HW-004** | Office Perimeter Network | HQ Cisco Meraki Firewalls, Switches, and Secure Wi-Fi APs | On-Premise HQ | IT Operations | Tier 3 | Internal | 802.1X authentication, WPA3-Enterprise, isolated guest VLAN |

---

## 4. Software & Cloud Services Inventory (ID.AM-02)

| Asset ID | Software / Service Name | Vendor / Publisher | Purpose | Deployment Type | Assigned Owner | Criticality | Data Handled |
|---|---|---|---|---|---|:---:|:---:|
| **SW-001** | Core Payment Gateway Engine | Proprietary (In-House) | Payment transaction processing, settlement calculation | Cloud Container (EKS) | Lead AppSec / CTO | Tier 1 | Restricted (Cardholder Data / PII) |
| **SW-002** | Customer Portal & Web App | Proprietary (In-House) | Customer onboarding, account management, UI | Cloud Container (EKS) | Lead Engineer | Tier 1 | Confidential (PII, Financial) |
| **SW-003** | PostgreSQL RDS Cluster | AWS RDS Aurora Multi-AZ | Primary transactional database | Cloud Managed DB | Lead Database Admin | Tier 1 | Restricted (Financial Records, Auth) |
| **SW-004** | Identity Provider & SSO | Okta | Single Sign-On and Adaptive MFA for corporate & cloud systems | SaaS | IT Security Lead | Tier 1 | Restricted (Credentials, User Directory) |
| **SW-005** | Customer CRM & Support | Salesforce | Customer service ticket tracking, contact management | SaaS | Head of Customer Ops | Tier 2 | Confidential (Customer Contacts) |
| **SW-006** | Google Workspace | Google | Corporate email, cloud document collaboration, team drives | SaaS | IT Operations | Tier 2 | Confidential (Business Communications) |
| **SW-007** | Endpoint Detection & Response | CrowdStrike Falcon | Real-time endpoint telemetry, behavioural malware detection | SaaS / Agent | IT Security Lead | Tier 1 | Internal (Telemetry & Logs) |
| **SW-008** | GitHub Enterprise | GitHub | Source code repository and automated CI/CD pipelines | SaaS | DevOps Lead | Tier 2 | Confidential (Source Code, IaC) |

---

## 5. Critical Data Repositories (ID.AM-03)

| Data Asset ID | Repository Name | Description | Host System | Data Classification | Retention Period | Applicable Regulations |
|---|---|---|---|:---:|---|---|
| **DAT-001** | Cardholder Token Vault | Tokenised payment identifiers, transaction authorization logs | AWS KMS + RDS DB | Restricted | 7 years | PCI DSS v4.0 |
| **DAT-002** | Customer Account Records | KYC profiles, government IDs, addresses, financial history | AWS Aurora RDS | Restricted | 5 years post-account closure | GDPR, AML / FCA Rules |
| **DAT-003** | System Audit & Security Logs | SIEM central event logs, CloudTrail, SSO authentication trails | AWS S3 (WORM Glacier) | Confidential | 1 year online, 7 years archive | SOC 2 (CC7), ISO 27001 (A.12.4) |
| **DAT-004** | Employee HR & Payroll Files | Staff contracts, bank accounts, performance and background checks | Workday / HR Drive | Confidential | Duration of employment + 6 yrs | Employment Law, GDPR |

---

## 6. Maintenance & Review Lifecycle

1. **Annual Complete Audit:** A formal physical and cloud asset reconciliation audit is performed annually prior to SOC 2 and ISO 27001 surveillance reviews.
2. **Change-Triggered Updates:** Any new software acquisition, cloud infrastructure provisioning, or hardware assignment must be logged in this register during the procurement and onboarding phase.
3. **Decommissioning & Sanitisation:** Hardware disposal follows NIST SP 800-88 sanitisation guidelines, accompanied by disposal certificates. Cloud storage buckets and database snapshots are securely wiped upon service termination.

---

*This document is a portfolio artefact created for a fictional fintech organisation (FinTech Co, 50 employees). All data schemas, asset configurations, and controls reflect real-world GRC documentation standards.*
