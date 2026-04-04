# NIST Cybersecurity Framework - Gap Analysis
**Organisation:** FinTech Co (Fictional - 50 employees)  
**Framework Version:** NIST CSF 2.0  
**Assessment Date:** March 2026  
**Prepared By:** GRC Analyst  
**Classification:** Internal - Confidential  

---

## Assessment Overview

This gap analysis evaluates FinTech Co's current security posture against the NIST Cybersecurity Framework (CSF) 2.0. For each function and subcategory, the current control state, maturity level, and recommended actions are documented.

**Maturity Scale:**

| Level | Label | Description |
|-------|-------|-------------|
| 0 | Not Implemented | No control exists |
| 1 | Initial | Ad hoc; undocumented; not consistently applied |
| 2 | Developing | Partially implemented; inconsistently applied |
| 3 | Defined | Documented and consistently applied |
| 4 | Managed | Measured, monitored, and regularly reviewed |
| 5 | Optimising | Continuously improved; benchmarked against industry |

**Target Maturity:** Level 3 (Defined) across all critical categories within 12 months.

---

## Function 1: GOVERN (GV)

*Establishes and monitors the organisation's cybersecurity risk management strategy, expectations, and policy.*

| ID | Subcategory | Current State | Maturity | Gap | Priority |
|----|------------|---------------|:--------:|-----|----------|
| GV.OC-01 | Organisational mission and cybersecurity risk strategy are established | Information Security Policy (POL-001) drafted; not yet formally ratified by board | 2 | Board-level ratification required; align policy to business objectives | 🟠 High |
| GV.OC-02 | Stakeholders with cybersecurity risk management roles are identified | CISO role exists; roles partially documented | 2 | Formalise RACI matrix; document all GRC roles and responsibilities | 🟠 High |
| GV.RM-01 | Risk management policy is established and communicated | Risk Register exists; formal policy not yet communicated to all staff | 2 | Complete risk policy communication; annual staff briefing required | 🟠 High |
| GV.RM-02 | Risk appetite and tolerance are determined and communicated | Risk appetite not formally documented | 1 | Define and document risk appetite statement; obtain executive sign-off | 🔴 Critical |
| GV.SC-01 | Supply chain risk management policy is established | Vendor questionnaire exists; formal policy absent | 1 | Develop TPRM policy; define critical vendor tiers and review schedule | 🔴 Critical |
| GV.PO-01 | Policy, process, and procedure lifecycle is established | Policies drafted; no formal review or approval lifecycle defined | 2 | Define policy lifecycle (owner, review period, approval authority) | 🟡 Medium |

---

## Function 2: IDENTIFY (ID)

*Helps the organisation understand its cybersecurity risk to systems, people, assets, data, and capabilities.*

| ID | Subcategory | Current State | Maturity | Gap | Priority |
|----|------------|---------------|:--------:|-----|----------|
| ID.AM-01 | Inventory of hardware assets is maintained | Partial asset inventory in a spreadsheet; not regularly updated | 2 | Implement asset management tool or CMDB; automate discovery | 🟠 High |
| ID.AM-02 | Inventory of software and services is maintained | No formal software inventory; shadow IT present | 1 | Conduct full software audit; implement approved software catalogue | 🔴 Critical |
| ID.AM-03 | Data assets, classifications, and flows are documented | Data Classification Policy drafted (POL-005); data flow map incomplete | 2 | Complete data flow mapping; include all third-party data flows | 🟠 High |
| ID.AM-07 | Inventories of IT and OT assets are maintained and prioritised | Asset criticality ratings absent | 1 | Add criticality and owner fields to asset inventory | 🟠 High |
| ID.RA-01 | Vulnerabilities are identified and documented | Annual vulnerability scan performed; no continuous scanning | 2 | Implement continuous vulnerability management; integrate with patch process | 🟠 High |
| ID.RA-02 | Cyber threat intelligence is consumed and analysed | No formal threat intelligence programme | 1 | Subscribe to FS-ISAC threat feeds; assign analyst to review monthly | 🟡 Medium |
| ID.RA-05 | Threats, vulnerabilities, likelihoods, and impacts are used to understand risk | Risk Register exists with L×I scoring; not yet integrated with asset inventory | 2 | Link Risk Register to asset inventory; conduct scenario-based risk analysis | 🟠 High |
| ID.IM-01 | Improvements from evaluations and lessons learned are identified | No formal lessons-learned process post-incident | 1 | Mandate post-incident reviews for P1/P2 events; track action items | 🟠 High |

---

## Function 3: PROTECT (PR)

*Supports the ability to limit or contain the impact of a cybersecurity event.*

| ID | Subcategory | Current State | Maturity | Gap | Priority |
|----|------------|---------------|:--------:|-----|----------|
| PR.AA-01 | Identities and credentials are managed | User accounts managed in Active Directory; no PAM solution | 2 | Implement PAM; enforce MFA for all privileged accounts | 🔴 Critical |
| PR.AA-02 | Identities are proofed and bound to credentials | Basic onboarding process; no formal identity verification for contractors | 2 | Formalise identity verification process for staff and contractors | 🟡 Medium |
| PR.AA-03 | Users, services, and hardware are authenticated | MFA enforced for VPN and admin consoles; gaps on some SaaS apps | 3 | Extend MFA to all SaaS applications via SSO integration | 🟠 High |
| PR.AA-05 | Access permissions are managed | RBAC partially implemented; access reviews done annually only | 2 | Move to quarterly access reviews; implement automated joiner-mover-leaver workflow | 🔴 Critical |
| PR.AT-01 | Personnel are provided awareness and training | Annual security awareness training; completion rate ~70% | 2 | Move to quarterly micro-trainings; mandate 100% completion; add phishing simulations | 🟠 High |
| PR.DS-01 | Data at rest is protected | Laptop encryption enforced; cloud data encryption partially configured | 2 | Audit all cloud storage encryption settings; enforce via policy and CSPM | 🟠 High |
| PR.DS-02 | Data in transit is protected | TLS 1.2 enforced on external services; internal traffic not fully encrypted | 2 | Audit internal traffic; enforce TLS 1.3 for all sensitive data flows | 🟠 High |
| PR.IR-01 | Networks and environments are protected | Basic network segmentation; no micro-segmentation in cloud | 2 | Implement VPC segmentation; define DMZ for public-facing services | 🟠 High |
| PR.PS-01 | Configuration management practices are maintained | Baseline hardening applied to servers; no CIS Benchmarks formally adopted | 2 | Adopt CIS Benchmark profiles; automate configuration compliance scanning | 🟡 Medium |
| PR.PS-02 | Software is maintained | Monthly patching cycle exists; critical patch SLA not enforced | 2 | Enforce 14-day critical patch SLA; track with vulnerability management tool | 🔴 Critical |

---

## Function 4: DETECT (DE)

*Enables timely discovery of cybersecurity events.*

| ID | Subcategory | Current State | Maturity | Gap | Priority |
|----|------------|---------------|:--------:|-----|----------|
| DE.AE-02 | Potentially adverse events are analysed | Basic SIEM logging; no dedicated analyst reviewing alerts | 1 | Assign alert triage responsibility; define alert escalation SLAs | 🔴 Critical |
| DE.AE-03 | Information is correlated from multiple sources | Logs collected from endpoints and cloud; not centralised or correlated | 1 | Consolidate logs into SIEM; build correlation rules for key attack patterns | 🔴 Critical |
| DE.AE-06 | A process for recording security events is established | Logging enabled on key systems; no consistent log standard | 2 | Define logging standard across all systems; audit for coverage gaps | 🟠 High |
| DE.CM-01 | Networks are monitored to find adverse events | No continuous network monitoring (IDS/IPS absent) | 1 | Evaluate IDS/IPS or NDR solution; begin with cloud-native tooling | 🟠 High |
| DE.CM-03 | Personnel activity and technology usage are monitored | Basic endpoint logging; no UEBA | 1 | Evaluate UEBA capability; prioritise for insider threat detection | 🟡 Medium |
| DE.CM-06 | External service provider activities are monitored | No monitoring of vendor access sessions | 1 | Implement privileged session recording for third-party access | 🟠 High |

---

## Function 5: RESPOND (RS)

*Supports the ability to contain the impact of a detected cybersecurity incident.*

| ID | Subcategory | Current State | Maturity | Gap | Priority |
|----|------------|---------------|:--------:|-----|----------|
| RS.MA-01 | Incident response plan is executed | Incident Response Policy (POL-004) drafted; not yet tested | 2 | Conduct tabletop exercise within 60 days of policy finalisation | 🔴 Critical |
| RS.MA-02 | Incidents are triaged and validated | Triage process documented in IRP; no playbooks for specific scenarios | 2 | Develop playbooks for ransomware, data breach, and phishing scenarios | 🟠 High |
| RS.CO-02 | Internal stakeholders are notified | IRT structure defined; no tested notification procedure | 2 | Run communications drill; confirm contact details for all IRT members | 🟠 High |
| RS.CO-03 | Information is shared with designated partners | No external sharing agreements (ISACs, regulators) | 1 | Join FS-ISAC; document regulatory notification process (GDPR 72hr rule) | 🟠 High |
| RS.AN-03 | Analysis is performed to establish root cause | No formal forensic capability; root cause analysis ad hoc | 1 | Document forensic evidence handling procedure; train Technical Lead | 🟠 High |

---

## Function 6: RECOVER (RC)

*Supports the timely restoration of normal operations to reduce the impact of a cybersecurity incident.*

| ID | Subcategory | Current State | Maturity | Gap | Priority |
|----|------------|---------------|:--------:|-----|----------|
| RC.RP-01 | Recovery plan is executed | BCP exists; DRP not formally documented | 1 | Document DRP with defined RTO/RPO; link to business impact analysis | 🔴 Critical |
| RC.RP-02 | Recovery plan is regularly updated | No scheduled review of BCP/DRP | 1 | Schedule annual BCP/DRP review; assign owner | 🟠 High |
| RC.RP-04 | Backups and restoration are tested | Backups run nightly; restore never tested | 1 | Schedule and complete quarterly restore test; document results | 🔴 Critical |
| RC.CO-03 | Recovery activities are communicated | No external communication plan for recovery phase | 1 | Develop customer and regulator communication templates for recovery | 🟡 Medium |

---

## Gap Summary

| Priority | Count | Key Themes |
|----------|------:|-----------|
| 🔴 Critical | 10 | Risk appetite, PAM, access reviews, SIEM/detection, patching, DRP, backup testing |
| 🟠 High | 17 | Asset inventory, MFA gaps, data encryption, logging, IRT testing, threat intel |
| 🟡 Medium | 5 | Configuration management, UEBA, identity proofing, recovery comms, policy lifecycle |
| **Total gaps** | **32** | |

---

## Recommended 12-Month Remediation Roadmap

### Immediate (0-90 days)
1. Document and obtain executive sign-off on risk appetite statement
2. Deploy PAM solution for privileged account management
3. Extend MFA to all SaaS applications via SSO
4. Centralise logging into SIEM with baseline correlation rules
5. Conduct first tabletop incident response exercise
6. Complete first quarterly restore test for backups
7. Document DRP with RTO/RPO targets

### Short-Term (3-6 months)
8. Implement continuous vulnerability scanning; enforce 14-day critical patch SLA
9. Complete software and asset inventory; remediate shadow IT
10. Develop IR playbooks (ransomware, data breach, phishing)
11. Join FS-ISAC; document GDPR 72-hour notification procedure
12. Move security awareness training to quarterly micro-format; target 100% completion

### Medium-Term (6-12 months)
13. Implement CSPM for cloud configuration monitoring
14. Complete data flow mapping including third-party flows
15. Evaluate and pilot UEBA capability
16. Implement network segmentation / micro-segmentation in cloud VPC
17. Establish formal TPRM policy and vendor risk tier system

---

*This gap analysis is a portfolio artefact created for a fictional fintech organisation (FinTech Co, 50 employees). All findings and recommendations reflect real-world GRC methodology applied to a representative small fintech environment.*
