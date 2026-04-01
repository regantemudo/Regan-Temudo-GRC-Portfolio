# Data Classification Policy

**Organisation:** FinTech Co  
**Document ID:** POL-005  
**Version:** 1.0  
**Effective Date:** March 2026  
**Review Date:** March 2027  
**Owner:** CISO / Data Protection Officer  
**Classification:** Internal  
**Framework Alignment:** ISO/IEC 27001 (A.8) | GDPR (Art. 5, 25) | PCI DSS (Req. 3, 9)

---

## 1. Purpose

This policy establishes a consistent framework for classifying FinTech Co's data assets based on their sensitivity and the potential impact of unauthorised disclosure, modification, or loss. Proper classification ensures that appropriate controls are applied proportionate to the risk.

---

## 2. Scope

This policy applies to all data created, received, stored, processed, or transmitted by FinTech Co regardless of format (digital, printed, verbal) or location (on-premise, cloud, mobile, remote).

---

## 3. Data Classification Levels

FinTech Co uses four classification levels:

---

### 🔴 Level 1: Restricted

**Definition:** The most sensitive data. Unauthorised disclosure would cause severe harm to customers, the business, or regulatory standing.

**Examples:**
- Payment card data (PAN, CVV, expiry dates) - PCI DSS in scope
- Authentication credentials (passwords, private keys, MFA seeds)
- Customer PII combined with financial data
- Vulnerability assessment reports and penetration test findings
- Merger, acquisition, or strategic business plans (pre-announcement)

**Handling Requirements:**
- Must be encrypted at rest (AES-256) and in transit (TLS 1.3)
- Access strictly limited to named, authorised individuals on a need-to-know basis
- Must not be transmitted via email without encryption
- Must not be stored on personal devices or unapproved cloud storage
- Printing requires prior authorisation; printed copies must be immediately secured and shredded when no longer needed
- Incidents involving Restricted data must be treated as P1 or P2 under the Incident Response Policy

---

### 🟠 Level 2: Confidential

**Definition:** Sensitive business or customer data. Unauthorised disclosure could cause significant operational, financial, or reputational harm.

**Examples:**
- Customer personal data (name, email, address, account number) not combined with financial data
- Employee records and HR data
- Internal financial reports and forecasts
- Vendor contracts and pricing agreements
- Audit findings and risk assessments (non-Restricted)
- Source code and technical architecture documents

**Handling Requirements:**
- Must be encrypted in transit (TLS 1.2 minimum)
- Must be stored on encrypted, access-controlled systems
- Sharing externally requires approval from the data owner
- Must not be shared via personal accounts or public channels
- Remote access requires VPN and MFA

---

### 🟡 Level 3: Internal

**Definition:** General internal business information not intended for public disclosure but with limited sensitivity.

**Examples:**
- Internal policies and procedures
- Project plans and internal meeting notes
- Organisational charts and team directories
- Non-sensitive internal communications

**Handling Requirements:**
- Must be stored on company-approved systems
- Must not be shared publicly or with unauthorised third parties
- Standard access controls apply
- No special encryption required beyond standard system controls

---

### 🟢 Level 4: Public

**Definition:** Information approved for public release. No restrictions on distribution.

**Examples:**
- Marketing materials and press releases
- Published product documentation
- Public-facing website content
- Job postings

**Handling Requirements:**
- No special handling controls required
- Must be reviewed and approved before publication to confirm it does not inadvertently contain Restricted, Confidential, or Internal data

---

## 4. Classification Responsibilities

| Role | Responsibility |
|------|---------------|
| **Data Creator / Owner** | Responsible for correctly classifying data at the point of creation and reviewing classification as needed |
| **All Staff** | Responsible for handling data in accordance with its classification level |
| **IT Security** | Responsible for implementing and maintaining technical controls that enforce classification requirements |
| **CISO / DPO** | Responsible for maintaining this policy and resolving classification disputes |

---

## 5. Labelling

- Digital documents containing Restricted or Confidential data must be clearly labelled with the classification level in the document header or footer.
- Emails containing Restricted or Confidential data must include the classification in the subject line (e.g. `[CONFIDENTIAL]`).
- Physical documents must be labelled on the cover page.

---

## 6. Data Retention & Disposal

| Classification | Minimum Retention | Disposal Method |
|---------------|-------------------|-----------------|
| Restricted | As required by regulation (e.g. PCI DSS: 1 year minimum for logs) | Secure deletion (NIST 800-88); physical shredding |
| Confidential | 7 years (financial); 6 years (contracts); as required by role | Secure deletion; cross-cut shredding |
| Internal | Duration of business need | Standard deletion |
| Public | Duration of business need | Standard deletion |

Disposal must be documented. Restricted data disposal requires sign-off from the data owner.

---

## 7. Special Categories of Personal Data (GDPR)

In addition to the classification levels above, special category personal data as defined under GDPR Article 9 (including health data, biometric data, racial or ethnic origin, and political opinions) must always be treated as **Restricted**, with explicit consent or a lawful basis documented prior to processing.

---

## 8. Related Documents

| Document | ID |
|----------|----|
| Information Security Policy | POL-001 |
| Access Control Policy | POL-003 |
| Incident Response Policy | POL-004 |
| Acceptable Use Policy | POL-002 |

---

## 9. Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | April 2026 | CISO | Initial release |

---

*This policy is a portfolio artefact created for a fictional fintech organisation (FinTech Co, 50 employees). Content reflects real-world GRC methodology aligned to ISO 27001 A.8, GDPR Articles 5 and 25, and PCI DSS Requirements 3 and 9.*
