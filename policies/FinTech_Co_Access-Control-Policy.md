# Access Control Policy

**Organisation:** FinTech Co  
**Document ID:** POL-003  
**Version:** 1.0  
**Effective Date:** March 2026  
**Review Date:** March 2027  
**Owner:** IT Security Manager  
**Classification:** Internal  
**Framework Alignment:** ISO/IEC 27001 (A.9) | NIST CSF (PR.AC) | SOC 2 (CC6)

---

## 1. Purpose

This policy defines how access to FinTech Co's information systems, applications, and data is granted, maintained, reviewed, and revoked. Its objective is to ensure that only authorised individuals have access to the resources they need to perform their roles and nothing more.

---

## 2. Scope

This policy applies to:

- All user accounts across all systems, applications, and cloud services operated by FinTech Co
- All employees, contractors, and third-party vendors with any level of system access
- Both human user accounts and non-human (service) accounts

---

## 3. Access Control Principles

### 3.1 Least Privilege

Access rights must be granted at the minimum level required for a user to perform their job function. Broad, blanket, or "admin by default" access is prohibited.

### 3.2 Need-to-Know

Users must only have access to data and systems directly relevant to their role. Access to sensitive data (e.g. customer PII, financial records) must be explicitly justified and approved.

### 3.3 Separation of Duties

Where possible, critical tasks must be split across two or more users to reduce the risk of fraud or error. No single individual should have end-to-end control of a sensitive process (e.g. initiating and approving a payment).

---

## 4. Access Provisioning

### 4.1 New User Onboarding

- Access requests must be submitted via the IT Service Desk using the approved Access Request Form.
- Requests must be approved by the user's line manager and, for elevated or privileged access, by the IT Security Manager.
- Access must be provisioned within 3 business days of a completed, approved request.
- Default access profiles (role-based templates) will be applied where available.

### 4.2 Role-Based Access Control (RBAC)

FinTech Co operates a role-based access control model. Defined role profiles include:

| Role Profile | Description |
|---|---|
| Standard User | Read/write access to business applications relevant to role |
| Finance User | Access to financial systems; restricted to Finance team |
| Developer | Access to development and staging environments; no prod write access by default |
| IT Administrator | Elevated system access; governed by PAM policy |
| Third-Party Vendor | Time-limited, scoped access approved case-by-case |

### 4.3 Privileged Access

- Privileged accounts (admin, root, service accounts) must be documented in the privileged access register.
- Privileged access must not be used for day-to-day tasks. Separate standard user accounts must be maintained.
- All privileged sessions must be logged.
- Just-in-time (JIT) access is the preferred model for privileged accounts where tooling supports it.

---

## 5. Authentication Requirements

- All accounts must be protected by a strong, unique password in accordance with the Password & Authentication Policy (POL-006).
- Multi-factor authentication (MFA) is mandatory for:
  - All remote access (VPN, remote desktop)
  - All cloud administration consoles
  - All privileged accounts
  - All access to systems storing sensitive or regulated data
- Single Sign-On (SSO) must be used where available to centralise authentication management.

---

## 6. Access Reviews

- Access rights for all users must be formally reviewed at least every 6 months.
- Privileged access must be reviewed quarterly.
- Reviews are conducted by line managers in collaboration with the IT Security team.
- Any access that cannot be justified must be revoked within 5 business days of the review.
- Review results must be documented and retained for audit purposes.

---

## 7. Access Modification & Revocation

### 7.1 Role Changes

When an employee changes role, their existing access must be reviewed within 5 business days. Access no longer required must be revoked; new access must follow the provisioning process in Section 4.

### 7.2 Offboarding

- All system access must be revoked on the employee's last working day (or immediately in the case of involuntary termination).
- IT must be notified of all departures by HR at least 3 business days in advance where possible.
- Physical access (keys, badges) must also be collected on departure.

### 7.3 Contractor & Vendor Access

- Third-party access must be time-limited and scoped to the minimum required.
- Access must be revoked immediately upon contract end.
- All third-party access must be logged and reviewed monthly.

---

## 8. Service Accounts & Non-Human Identities

- All service accounts must be inventoried and assigned a human owner.
- Service account credentials must not be shared or embedded in code. Use secrets management tooling (e.g. Vault, AWS Secrets Manager).
- Service accounts must follow the same least-privilege and review requirements as human accounts.

---

## 9. Audit & Logging

- All authentication events (successes and failures) must be logged.
- Failed login attempts exceeding 5 consecutive failures must trigger an alert and temporary account lockout.
- Logs must be retained for a minimum of 12 months and reviewed regularly for anomalous patterns.

---

## 10. Related Documents

| Document | ID |
|----------|----|
| Information Security Policy | POL-001 |
| Password & Authentication Policy | POL-006 |
| Incident Response Policy | POL-004 |
| Data Classification Policy | POL-005 |

---

## 11. Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | IT Security Manager | Initial release |

---

*This policy is a portfolio artefact created for a fictional fintech organisation (FinTech Co, 50 employees). Content reflects real-world GRC methodology aligned to ISO 27001 Annex A.9, NIST CSF PR.AC, and SOC 2 CC6.*
