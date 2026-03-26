# Information Security Risk Register
**Organisation:** FinTech Co (Fictional - 50 employees)  
**Framework Alignment:** ISO/IEC 27001 | NIST Cybersecurity Framework  
**Last Reviewed:** March 2026  
**Owner:** CISO / GRC Lead  

---

## Scoring Methodology

**Risk Score = Likelihood × Impact**

| Score | Likelihood | Impact |
|-------|-----------|--------|
| 1 | Rare | Negligible |
| 2 | Unlikely | Minor |
| 3 | Possible | Moderate |
| 4 | Likely | Major |
| 5 | Almost Certain | Catastrophic |

| Rating | Score Range |
|--------|-------------|
| 🔴 Critical | 16 - 25 |
| 🟠 High | 10 - 15 |
| 🟡 Medium | 6 - 9 |
| 🟢 Low | 1 - 5 |

---

## Risk Register

### Category: Cyber / Data Breach

| Risk ID | Risk Title | Description | Affected Asset | Threat Source | Likelihood | Impact | Score | Rating | Current Controls | Treatment | Recommended Action | Owner |
|---------|-----------|-------------|---------------|--------------|:----------:|:------:|:-----:|--------|-----------------|-----------|-------------------|-------|
| R-001 | Ransomware Attack | Malicious encryption of systems and data demanding ransom payment | Payment processing systems, customer PII | External threat actor | 4 | 5 | **20** | 🔴 Critical | Endpoint AV, email filtering | Mitigate | Deploy EDR solution; enforce offline backups; conduct phishing simulation | CISO |
| R-002 | Customer Data Breach via Web App | Exploitation of web application vulnerability exposing cardholder and PII data | Customer portal, payment API | External attacker | 3 | 5 | **15** | 🟠 High | WAF, input validation, TLS | Mitigate | Conduct quarterly DAST/SAST; implement bug bounty programme | AppSec Lead |
| R-003 | Insider Data Theft | Malicious or negligent employee exfiltrates sensitive customer or financial data | CRM, financial records, PII database | Malicious insider | 2 | 5 | **10** | 🟠 High | DLP tool, role-based access | Mitigate | Implement UEBA; enforce least privilege; quarterly access reviews | IT Security |
| R-004 | Phishing / Credential Compromise | Employee credentials stolen via phishing, enabling unauthorised system access | Email, SaaS applications, VPN | External attacker | 4 | 4 | **16** | 🔴 Critical | MFA on critical systems, security awareness training | Mitigate | Enforce MFA across all systems; deploy anti-phishing email gateway | IT Manager |
| R-005 | Unpatched Software Vulnerability | Exploitation of known CVEs in unpatched servers or applications | Web servers, internal applications | External attacker | 3 | 4 | **12** | 🟠 High | Monthly patching cycle | Mitigate | Implement vulnerability management programme; target 14-day critical patch SLA | IT Ops |
| R-018 | API Security Misconfiguration | Internal or external APIs expose excessive data or lack proper authentication | Customer data, payment integrations | External attacker | 3 | 4 | **12** | 🟠 High | Basic API keys in use | Mitigate | Implement OAuth 2.0 / API gateway; conduct annual API security review | AppSec Lead |

---

### Category: Third-Party / Vendor Risk

| Risk ID | Risk Title | Description | Affected Asset | Threat Source | Likelihood | Impact | Score | Rating | Current Controls | Treatment | Recommended Action | Owner |
|---------|-----------|-------------|---------------|--------------|:----------:|:------:|:-----:|--------|-----------------|-----------|-------------------|-------|
| R-006 | Payment Processor Outage | Critical payment gateway provider suffers downtime, halting transaction processing | Payment processing, revenue | Third-party vendor | 2 | 5 | **10** | 🟠 High | SLA in contract, secondary processor identified | Transfer | Activate secondary payment processor; review SLA penalties with legal | CFO / Ops |
| R-007 | Vendor Data Breach (4th Party) | A key vendor suffers a breach exposing data shared by FinTech Co | Shared customer data, API integrations | Third-party vendor | 3 | 5 | **15** | 🟠 High | Annual vendor security questionnaire | Mitigate | Implement TPRM programme; require SOC 2 Type II reports from critical vendors | Procurement |
| R-008 | Cloud Provider Misconfiguration | Misconfigured AWS/GCP settings expose storage buckets or services publicly | Cloud infrastructure, stored data | Internal error / vendor | 3 | 4 | **12** | 🟠 High | IaC templates, basic CSPM alerts | Mitigate | Deploy CSPM tool (e.g. Wiz/Prisma); enforce infrastructure-as-code reviews | Cloud Architect |
| R-009 | Vendor Contract Non-Compliance | Critical SaaS vendor fails to meet regulatory or data handling contractual obligations | Data processing agreements, compliance posture | Third-party vendor | 2 | 3 | **6** | 🟡 Medium | DPAs in place for key vendors | Mitigate | Annual DPA review; align contracts with GDPR/PCI DSS obligations | Legal / Compliance |
| R-019 | Open Source Software Vulnerability | Unvetted open-source library contains malicious code or critical CVE | Application codebase, build pipeline | Supply chain / external | 3 | 4 | **12** | 🟠 High | No formal SCA in place | Mitigate | Integrate SCA tool (e.g. Snyk/Dependabot) into CI/CD pipeline | Engineering Lead |

---

### Category: Operational / People Risk

| Risk ID | Risk Title | Description | Affected Asset | Threat Source | Likelihood | Impact | Score | Rating | Current Controls | Treatment | Recommended Action | Owner |
|---------|-----------|-------------|---------------|--------------|:----------:|:------:|:-----:|--------|-----------------|-----------|-------------------|-------|
| R-010 | Key Person Dependency | Critical security or IT knowledge concentrated in one or two individuals | Security operations, system administration | Internal — people | 3 | 4 | **12** | 🟠 High | Some documentation exists | Mitigate | Document all critical processes; cross-train backup staff; implement succession planning | HR / CISO |
| R-011 | Accidental Data Deletion | Employee accidentally deletes critical database or configuration files | Databases, configuration management | Internal — human error | 3 | 4 | **12** | 🟠 High | Daily automated backups | Mitigate | Implement soft-delete / versioning; test restore procedures quarterly | IT Ops |
| R-012 | Inadequate Security Awareness | Employees unaware of security policies, leading to policy violations or incidents | All systems and data | Internal — human error | 4 | 3 | **12** | 🟠 High | Annual security awareness training | Mitigate | Move to quarterly micro-trainings; track completion; simulate phishing monthly | HR / Security |
| R-013 | Unauthorised Shadow IT | Employees use unapproved SaaS tools storing company or customer data | Data governance, compliance posture | Internal — people | 3 | 3 | **9** | 🟡 Medium | Acceptable use policy exists | Mitigate | Deploy CASB; publish approved software catalogue; enforce policy with HR | IT Security |
| R-020 | Privileged Access Abuse | Admin accounts used without oversight; excessive privileges granted and not revoked | All systems, databases, cloud infrastructure | Internal — people | 2 | 4 | **8** | 🟡 Medium | Some access reviews done annually | Mitigate | Implement PAM solution; enforce just-in-time access; quarterly privilege reviews | IT Security |

---

### Category: Business Continuity / DR

| Risk ID | Risk Title | Description | Affected Asset | Threat Source | Likelihood | Impact | Score | Rating | Current Controls | Treatment | Recommended Action | Owner |
|---------|-----------|-------------|---------------|--------------|:----------:|:------:|:-----:|--------|-----------------|-----------|-------------------|-------|
| R-014 | Data Centre / Primary Cloud Region Failure | Primary hosting environment becomes unavailable due to outage or disaster | All hosted services, customer-facing applications | Natural disaster / infra failure | 2 | 5 | **10** | 🟠 High | Single-region deployment with snapshots | Mitigate | Design multi-region active-passive architecture; test failover bi-annually | CTO / Cloud Arch |
| R-015 | Backup Failure / Data Loss | Backup processes fail silently; data unrecoverable during incident | All critical data assets | Internal — process failure | 2 | 5 | **10** | 🟠 High | Automated nightly backups (untested) | Mitigate | Implement backup monitoring with alerts; schedule quarterly restore tests | IT Ops |
| R-016 | Business Continuity Plan Not Tested | BCP exists on paper but has never been exercised; real invocation likely to fail | All business operations | Internal — governance gap | 3 | 4 | **12** | 🟠 High | BCP document in place | Mitigate | Conduct tabletop exercise within 90 days; schedule annual full DR test | COO / CISO |
| R-017 | Extended Power / Internet Outage | Office or co-location facility loses power or connectivity for extended period | Office operations, on-prem systems | External — infrastructure | 2 | 3 | **6** | 🟡 Medium | UPS units in office | Accept | Document remote-work fallback procedure; consider cloud-first migration | IT Manager |

---

## Risk Summary

| Rating | Count | Risk IDs |
|--------|------:|---------|
| 🔴 Critical | 2 | R-001, R-004 |
| 🟠 High | 13 | R-002, R-003, R-005, R-006, R-007, R-008, R-010, R-011, R-012, R-014, R-015, R-016, R-019 |
| 🟡 Medium | 4 | R-009, R-013, R-017, R-020 |
| 🟢 Low | 0 | - |
| **Total** | **20** | |

---

## Treatment Summary

| Treatment | Count |
|-----------|------:|
| Mitigate | 18 |
| Transfer | 1 |
| Accept | 1 |
| Avoid | 0 |

---

*This risk register is a portfolio artefact created for demonstration purposes using a fictional fintech organisation. All risks, controls, and recommendations reflect real-world GRC methodology.*
