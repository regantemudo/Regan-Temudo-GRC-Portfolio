# Executive Risk Brief: Ransomware Threat to FinTech Co

**Brief ID:** EB-001  
**Date:** March 2026  
**Prepared By:** GRC Analyst  
**Audience:** CEO, CFO, Board Risk Committee  
**Classification:** Confidential  
**Risk Reference:** R-001 (Risk Register)

---

## Situation Summary

Ransomware attacks against financial services organisations have increased significantly over the past two years. FinTech Co's current security controls  while functional contain gaps that leave the organisation materially exposed. This brief summarises the risk, its potential business impact, and the actions recommended for leadership consideration.

---

## What Is the Risk?

Ransomware is malicious software that encrypts an organisation's systems and data, rendering them inaccessible. Attackers demand a ransom payment  typically in cryptocurrency  in exchange for a decryption key. Even when the ransom is paid, recovery is not guaranteed.

Attackers typically enter through phishing emails, unpatched systems, or compromised credentials. FinTech Co currently scores this risk as **Critical (score: 20/25)**  the highest rating in our Risk Register.

---

## Why FinTech Co Is Exposed

Three specific gaps increase our exposure:

**1. No endpoint detection and response (EDR) solution is deployed.** Our current antivirus provides signature-based detection only. Modern ransomware variants evade signature detection routinely. EDR provides behavioural monitoring that can detect and stop ransomware before it spreads.

**2. Backup restores have never been tested.** We run nightly backups, but have never confirmed that a full restore is possible. In a ransomware scenario, an untested backup is not a recovery strategy it is a hope.

**3. Phishing simulation has never been conducted.** Ransomware most commonly enters via phishing. Without knowing how our staff respond to phishing attempts, we cannot assess our real-world exposure through the human layer.

---

## Potential Business Impact

| Impact Area | Estimated Exposure |
|-------------|-------------------|
| Operational downtime | 2–4 weeks to recover without a tested DRP |
| Revenue loss | Estimated £150,000–£400,000 depending on duration |
| Regulatory penalties | GDPR fines up to 4% of annual global turnover if personal data is exfiltrated |
| Reputational damage | Loss of customer trust; potential churn from enterprise accounts |
| Ransom demand | Typically £50,000–£500,000 for organisations of our size |

A ransomware incident at FinTech Co could realistically result in **£500,000–£1,000,000 in total losses** when operational, regulatory, and reputational costs are combined — before any ransom payment.

---

## Recommended Actions

The following three actions would materially reduce FinTech Co's ransomware exposure within 90 days:

| Action | Estimated Cost | Effort | Risk Reduction |
|--------|---------------|--------|----------------|
| Deploy EDR solution (e.g. CrowdStrike Falcon Go or SentinelOne) | £8,000–£15,000/year | Low - vendor-managed | High |
| Conduct quarterly backup restore test | Minimal (internal IT time) | Low | High |
| Launch monthly phishing simulation programme | £3,000–£6,000/year | Low - vendor-managed | Medium–High |

These three actions are estimated to reduce the risk score from **Critical (20)** to **High (12)** within one quarter.

---

## Recommended Decision

> **Leadership is asked to approve budget for EDR deployment and phishing simulation programme, and to mandate a backup restore test within 30 days.**

The combined annual investment of approximately **£15,000-£21,000** is significantly below the estimated minimum loss exposure of **£500,000** in the event of an incident.

---

## Next Steps

| Action | Owner | Timeline |
|--------|-------|----------|
| Approve EDR vendor evaluation | CISO | 2 weeks |
| Schedule backup restore test | IT Manager | 30 days |
| Approve phishing simulation vendor | CISO | 4 weeks |
| Brief all staff on ransomware awareness | HR / Security | 6 weeks |

---

*This brief was prepared by the GRC function for senior leadership. Supporting technical detail is available on request. Risk ratings reference the FinTech Co Information Security Risk Register (March 2026).*

---

*This document is a portfolio artefact created for a fictional fintech organisation (FinTech Co, 50 employees). All figures and scenarios are illustrative and reflect real-world GRC communication methodology.*

