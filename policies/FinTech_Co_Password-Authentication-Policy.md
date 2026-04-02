# Password & Authentication Policy

**Organisation:** FinTech Co  
**Document ID:** POL-006  
**Version:** 1.0  
**Effective Date:** April 2026  
**Review Date:** April 2027  
**Owner:** IT Security Manager  
**Classification:** Internal  
**Framework Alignment:** ISO/IEC 27001 (A.9.4) | NIST SP 800-63B | PCI DSS (Req. 8)

---

## 1. Purpose

This policy establishes FinTech Co's requirements for passwords and authentication mechanisms used to access company systems and data. It aims to protect against unauthorised access resulting from weak, reused, or compromised credentials.

---

## 2. Scope

This policy applies to all user accounts human and non-human across all FinTech Co systems, applications, and cloud services, including those accessed by employees, contractors, and third-party vendors.

---

## 3. Password Requirements

### 3.1 Standard User Accounts

All passwords for standard user accounts must meet the following minimum requirements:

| Requirement | Standard |
|-------------|----------|
| Minimum length | 12 characters |
| Complexity | At least one uppercase letter, one lowercase letter, one number, and one special character |
| Maximum age | 12 months (or immediately upon suspected compromise) |
| History | Cannot reuse the last 10 passwords |
| Lockout | Account locked after 10 consecutive failed attempts |
| Lockout duration | 30 minutes, or until unlocked by IT |

### 3.2 Privileged & Administrative Accounts

Accounts with elevated or administrative privileges must meet stricter requirements:

| Requirement | Standard |
|-------------|----------|
| Minimum length | 16 characters |
| Complexity | As above |
| Maximum age | 90 days |
| MFA | Mandatory - no exceptions |
| Lockout | Account locked after 5 consecutive failed attempts |

### 3.3 NIST-Aligned Guidance

In line with NIST SP 800-63B, FinTech Co applies the following practices:

- Passwords are checked against known breached credential lists at the point of creation or reset.
- Users are not required to change passwords on a fixed schedule unless compromise is suspected. The 12-month maximum age applies as an outer bound.
- Password complexity requirements apply, but users are encouraged to use passphrases (e.g. four or more random words) as these are both stronger and more memorable.
- Password hints and security questions must not be used as authentication mechanisms.

---

## 4. Multi-Factor Authentication (MFA)

MFA is required for all of the following:

- Remote access to company systems (VPN, remote desktop)
- All cloud administration consoles (AWS, GCP, Microsoft 365 admin)
- All privileged accounts
- Access to systems storing Restricted or Confidential data (as defined in POL-005)
- All SaaS applications that store company or customer data where MFA is supported

**Approved MFA methods** (in order of preference):

1. FIDO2 / hardware security key (e.g. YubiKey) preferred
2. Authenticator app (e.g. Microsoft Authenticator, Google Authenticator) - TOTP
3. Push notification via approved app

**Prohibited MFA methods:**

- SMS-based one-time passwords (OTP) - not permitted for Restricted data systems due to SIM-swap risk
- Email-based OTP - not permitted for privileged account access

---

## 5. Password Manager

- Employees must use the company-approved password manager to generate and store unique passwords.
- Passwords must not be stored in browsers, spreadsheets, notes apps, or any unapproved tool.
- The master password for the password manager must meet the requirements in Section 3.2 and must not be reused elsewhere.

---

## 6. Credential Hygiene

Users must:

- Never share passwords with anyone, including IT staff. FinTech Co IT will never ask for a password.
- Never use the same password across multiple systems or accounts.
- Never write passwords down or store them in plaintext.
- Immediately report suspected credential compromise to IT Security and change affected passwords at once.
- Not use personal passwords for work systems, or work passwords for personal accounts.

---

## 7. Service & System Accounts

- Service account credentials must not be hardcoded in source code, configuration files, or scripts.
- Secrets must be stored in an approved secrets management tool (e.g. HashiCorp Vault, AWS Secrets Manager).
- Service account passwords must meet the requirements in Section 3.2 and must be rotated at least every 90 days, or immediately if a team member with access departs.
- All service accounts must have a named human owner.

---

## 8. Temporary Passwords & Initial Credentials

- Temporary passwords issued for new accounts or password resets must be unique, time-limited (expiry within 24 hours), and force a change on first login.
- Temporary credentials must be transmitted via a secure channel - never in the same communication as the account details.

---

## 9. Monitoring & Enforcement

- Systems must be configured to enforce the requirements in this policy technically where possible.
- Failed login attempts must be logged and alerted on when thresholds are exceeded.
- IT Security will periodically test password quality across key systems.
- Non-compliance with this policy may result in account suspension and disciplinary action.

---

## 10. Related Documents

| Document | ID |
|----------|----|
| Information Security Policy | POL-001 |
| Access Control Policy | POL-003 |
| Acceptable Use Policy | POL-002 |
| Data Classification Policy | POL-005 |

---

## 11. Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | IT Security Manager | Initial release |

---

*This policy is a portfolio artefact created for a fictional fintech organisation (FinTech Co, 50 employees). Content reflects real-world GRC methodology aligned to ISO 27001 A.9.4, NIST SP 800-63B, and PCI DSS Requirement 8.*
