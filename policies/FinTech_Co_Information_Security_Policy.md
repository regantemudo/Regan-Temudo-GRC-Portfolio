# Information Security Policy

**Organisation:** FinTech Co  
**Document ID:** POL-001  
**Version:** 1.0  
**Effective Date:** March 2026  
**Review Date:** March 2027  
**Owner:** Chief Information Security Officer (CISO)  
**Classification:** Internal  
**Framework Alignment:** ISO/IEC 27001 | NIST CSF

---

## 1. Purpose

This policy establishes FinTech Co's commitment to protecting the confidentiality, integrity, and availability of all information assets. It defines the minimum security requirements applicable to all staff, systems, and third parties handling company or customer data.

---

## 2. Scope

This policy applies to:

- All employees, contractors, and third-party vendors with access to FinTech Co systems or data
- All information assets owned, managed, or processed by FinTech Co
- All environments including cloud, on-premise, and remote working setups

---

## 3. Policy Statements

### 3.1 Governance & Accountability

- The CISO is responsible for maintaining and enforcing this policy.
- All employees must complete information security awareness training upon onboarding and annually thereafter.
- Policy violations will be reviewed and may result in disciplinary action up to and including termination.

### 3.2 Risk Management

- FinTech Co will conduct a formal risk assessment at least annually, or following significant changes to the business or technology environment.
- Identified risks will be recorded in the Risk Register and assigned an owner responsible for implementing treatment plans.
- Risk acceptance decisions must be documented and approved by the CISO.

### 3.3 Asset Management

- All information assets must be inventoried, classified, and assigned an owner.
- Assets must be handled in accordance with the Data Classification Policy (POL-005).
- Unneeded data must be securely disposed of using approved methods.

### 3.4 Access Control

- Access to systems and data must be granted on a least-privilege basis.
- All user accounts must be unique - shared accounts are prohibited.
- Privileged access must be reviewed quarterly and revoked promptly upon role change or departure.
- Multi-factor authentication (MFA) is mandatory for all remote access and privileged accounts.

### 3.5 Cryptography

- Sensitive data must be encrypted at rest (AES-256 minimum) and in transit (TLS 1.2 or higher).
- Encryption keys must be managed through a documented key management process and rotated annually.

### 3.6 Physical & Environmental Security

- Access to areas housing sensitive systems must be restricted to authorised personnel only.
- Clean desk and clear screen practices must be observed in all office environments.

### 3.7 Operations Security

- All systems must be covered by a patch management schedule. Critical vulnerabilities must be remediated within 14 days of disclosure.
- Anti-malware controls must be deployed and maintained on all endpoints.
- System logs must be retained for a minimum of 12 months and reviewed regularly for anomalies.

### 3.8 Supplier Relationships

- Third-party vendors with access to FinTech Co data or systems must sign a Data Processing Agreement (DPA) and complete an annual security assessment.
- Critical suppliers must demonstrate compliance with ISO 27001 or provide a current SOC 2 Type II report.

### 3.9 Incident Management

- All suspected security incidents must be reported to the security team immediately via the incident reporting channel.
- Incidents will be managed in accordance with the Incident Response Policy (POL-004).
- Post-incident reviews must be conducted for all High or Critical severity events.

### 3.10 Business Continuity

- FinTech Co will maintain a Business Continuity Plan (BCP) and Disaster Recovery Plan (DRP) aligned to defined Recovery Time Objectives (RTOs) and Recovery Point Objectives (RPOs).
- BCP and DRP tests must be conducted at least annually.

---

## 4. Exceptions

Exceptions to this policy must be requested in writing, reviewed by the CISO, and formally approved and documented. All approved exceptions are time-limited and subject to annual review.

---

## 5. Compliance & Enforcement

Compliance with this policy is mandatory. Non-compliance may result in disciplinary action. Repeated or wilful violations may be escalated to senior management or legal counsel.

---

## 6. Related Documents

| Document | ID |
|----------|----|
| Acceptable Use Policy | POL-002 |
| Access Control Policy | POL-003 |
| Incident Response Policy | POL-004 |
| Data Classification Policy | POL-005 |
| Password & Authentication Policy | POL-006 |
| Risk Register | risk-assessment/Risk_Register_FinTechCo.md |

---

## 7. Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | CISO | Initial release |

---

*This policy is a portfolio artefact created for a fictional fintech organisation (FinTech Co, 50 employees). All content reflects real-world GRC methodology aligned to ISO 27001 and NIST CSF.*
