# Incident Response Policy

**Organisation:** FinTech Co  
**Document ID:** POL-004  
**Version:** 1.0  
**Effective Date:** March 2026  
**Review Date:** March 2027  
**Owner:** CISO  
**Classification:** Internal - Restricted  
**Framework Alignment:** ISO/IEC 27001 (A.16) | NIST CSF (RS) | GDPR (Art. 33–34)

---

## 1. Purpose

This policy establishes FinTech Co's approach to identifying, managing, and recovering from information security incidents. It ensures that incidents are handled in a consistent, timely, and legally compliant manner minimising harm to customers, the business, and its reputation.

---

## 2. Scope

This policy applies to all security incidents affecting FinTech Co systems, data, or personnel, including:

- Suspected or confirmed data breaches
- Malware or ransomware infections
- Unauthorised access to systems or data
- Denial of service attacks
- Insider threats or policy violations
- Physical security breaches affecting information assets
- Third-party incidents impacting FinTech Co data

---

## 3. Incident Severity Classification

| Severity | Criteria | Example | Response SLA |
|----------|----------|---------|-------------|
| **P1 - Critical** | Active breach, significant data exposure, major service outage | Ransomware outbreak, customer PII exfiltrated | Immediate - 15 min |
| **P2 - High** | Confirmed attack, limited breach, high risk of escalation | Compromised admin account, targeted phishing | 1 hour |
| **P3 - Medium** | Suspicious activity, potential incident, limited impact | Failed intrusion attempt, malware on endpoint | 4 hours |
| **P4 - Low** | Policy violation, low-risk anomaly, single user impact | Weak password use, minor AUP breach | Next business day |

---

## 4. Incident Response Team

| Role | Responsibility |
|------|---------------|
| **Incident Commander** | CISO - leads response, makes escalation decisions |
| **Technical Lead** | IT Security Manager - leads containment and investigation |
| **Communications Lead** | Head of Legal / Compliance - manages regulatory and external comms |
| **Business Lead** | COO - coordinates business continuity during incident |
| **HR Representative** | Involved for incidents with insider threat or staff impact |

For P1/P2 incidents, the Incident Response Team (IRT) convenes within 1 hour of declaration.

---

## 5. Incident Response Process

### Phase 1 - Detection & Reporting

- Any employee who suspects or observes a security incident must report it immediately to the IT Security team via:
  - **Email:** security@fintechco.internal
  - **Slack:** #security-incidents channel
  - **Phone:** IT Security on-call number (out of hours)
- Reports must include: what was observed, when, on which system, and any actions already taken.
- IT Security will perform an initial triage within 30 minutes of receipt to determine if the event constitutes an incident and assign a severity level.

### Phase 2 - Containment

- Immediate containment actions must be taken to prevent further damage. These may include:
  - Isolating affected systems from the network
  - Revoking compromised credentials
  - Blocking malicious IP addresses or domains
  - Suspending affected user accounts
- Containment actions must be documented in real time in the Incident Log.
- Evidence must be preserved where possible affected systems should not be wiped or rebuilt until forensic requirements are confirmed.

### Phase 3 - Investigation & Analysis

- The Technical Lead will conduct a root cause analysis to determine:
  - How the incident occurred (attack vector, vulnerability exploited)
  - What data or systems were affected
  - The timeline of attacker activity
  - Whether the incident is contained or ongoing
- Findings must be documented in the Incident Report.

### Phase 4 - Eradication

- Once the root cause is identified, the threat must be fully removed:
  - Malware removed and affected systems rebuilt or restored from clean backups
  - Compromised credentials reset across all affected systems
  - Exploited vulnerabilities patched or mitigated
  - Indicators of Compromise (IoCs) blocked at the perimeter

### Phase 5 - Recovery

- Systems are restored to normal operation following confirmation that the threat is eradicated.
- Restoration must be tested before returning systems to production.
- Enhanced monitoring must be applied to previously affected systems for a minimum of 30 days post-recovery.

### Phase 6 - Post-Incident Review

- A Post-Incident Review (PIR) must be conducted for all P1 and P2 incidents within 10 business days of closure.
- The PIR must cover:
  - Incident timeline and root cause
  - Effectiveness of the response
  - Lessons learned
  - Remediation actions with owners and deadlines
- PIR findings must be shared with senior leadership and used to improve controls and this policy.

---

## 6. Regulatory Notification Requirements

### GDPR (Personal Data Breaches)

- If a personal data breach is confirmed, the CISO and Legal must assess the risk to data subjects within 24 hours.
- If notification is required, the relevant Data Protection Authority must be notified within **72 hours** of becoming aware of the breach.
- Affected data subjects must be notified without undue delay if the breach is likely to result in high risk to their rights and freedoms.
- Notification records must be retained regardless of whether a report is made.

### PCI DSS

- Any suspected breach involving payment card data must trigger immediate notification to the relevant card brands and acquiring bank in accordance with PCI DSS incident response requirements.

---

## 7. Evidence Handling & Chain of Custody

- All evidence collected during an incident (logs, disk images, screenshots) must be logged with: what was collected, when, by whom, and how it is stored.
- Evidence must not be altered. Work from copies where possible.
- Chain of custody documentation must be maintained for any evidence that may be used in legal proceedings.

---

## 8. Communication Guidelines

- Internal communications regarding an active incident must be limited to those with a need to know.
- External communications (press, customers, regulators) must be approved by the Communications Lead before release.
- Employees must not discuss active incidents on social media or with third parties outside of the approved communications process.

---

## 9. Testing & Training

- The Incident Response Plan must be tested at least annually via a tabletop exercise.
- All members of the Incident Response Team must participate in annual IR training.
- Lessons from exercises must be incorporated into this policy and related procedures.

---

## 10. Related Documents

| Document | ID |
|----------|----|
| Information Security Policy | POL-001 |
| Business Continuity Plan | BCP-001 |
| Data Classification Policy | POL-005 |
| Risk Register | risk-assessment/Risk_Register_FinTechCo.md |

---

## 11. Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | CISO | Initial release |

---

*This policy is a portfolio artefact created for a fictional fintech organisation (FinTech Co, 50 employees). Content reflects real-world GRC methodology aligned to ISO 27001 A.16, NIST CSF Response function, and GDPR Articles 33-34.*
