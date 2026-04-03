# Executive Risk Brief: Third-Party Vendor Risk Exposure

**Brief ID:** EB-002  
**Date:** April 2026  
**Prepared By:** GRC Analyst  
**Audience:** CEO, COO, Head of Legal  
**Classification:** Confidential  
**Risk Reference:** R-007, R-009, R-019 (Risk Register)

---

## Situation Summary

FinTech Co relies on approximately 15–20 third-party vendors for critical business operations, including payment processing, cloud infrastructure, HR systems, and customer communication tools. Our current approach to managing vendor security risk is informal and inconsistent. This brief outlines the exposure this creates and recommends a proportionate response.

---

## The Risk in Plain Terms

When we share customer data with a vendor or rely on a vendor to process payments on our behalf their security posture becomes our risk. If a vendor is breached, we may face the same regulatory, legal, and reputational consequences as if we had been breached directly.

Under GDPR, FinTech Co remains the **data controller** even when a vendor processes data on our behalf. This means we are accountable for how that vendor handles our customers' personal data regardless of what caused their breach.

Our three highest-rated vendor risks are:

- **R-007 - Vendor Data Breach (4th Party):** A key vendor suffers a breach that exposes FinTech Co customer data. Currently rated **High (15/25).**
- **R-009 - Vendor Contract Non-Compliance:** A SaaS vendor fails to meet contractual or data handling obligations. Rated **Medium (6/25).**
- **R-019 - Open Source Software Vulnerability:** An unvetted open-source component introduces a critical vulnerability into our product. Rated **High (12/25).**

---

## What We Currently Do

| Control | Status |
|---------|--------|
| Annual vendor security questionnaire | Completed for 4 of ~18 vendors |
| Data Processing Agreements (DPAs) | In place for ~60% of vendors handling personal data |
| SOC 2 / ISO 27001 verification | Not consistently requested or reviewed |
| Vendor access monitoring | Not in place |
| Critical vendor tier classification | Not defined |

**In short:** Our vendor risk management is reactive and incomplete. We have not formally classified which vendors are critical, and we have no consistent process for assessing their security posture before onboarding or during the relationship.

---

## Potential Business Impact

A breach at a key vendor particularly our payment processor or cloud provider — could result in:

| Impact Area | Exposure |
|-------------|---------|
| GDPR regulatory fine | Up to 4% of annual global turnover |
| Customer notification costs | £20,000–£60,000 (legal, communications, credit monitoring) |
| Payment processing downtime | Revenue loss of £5,000–£25,000 per day depending on duration |
| Reputational damage | Difficult to quantify; material risk to customer retention |
| Legal liability | Potential civil claims from affected customers |

Critically, under GDPR Article 83, ignorance of a vendor's security practices is not a mitigating factor. Regulators expect data controllers to have performed due diligence on processors.

---

## What a Basic TPRM Programme Looks Like

A Third-Party Risk Management (TPRM) programme does not need to be complex to be effective at our scale. For a 50-person fintech, the following is practical and proportionate:

**1. Classify vendors into tiers by criticality:**

| Tier | Criteria | Review Frequency |
|------|----------|-----------------|
| Critical | Access to customer PII or payment data; essential to operations | Annual full assessment + SOC 2 Type II review |
| Important | Business productivity tools; limited data access | Annual questionnaire |
| Standard | Low-data or non-sensitive tools | Onboarding check only |

**2. Minimum requirements for Critical vendors:**
- Signed DPA before data sharing begins
- Annual completion of security questionnaire
- Current SOC 2 Type II report or equivalent (ISO 27001 certification)
- Contractual right to audit

**3. Offboarding process:** Confirm data deletion and access revocation when a vendor relationship ends.

---

## Recommended Actions

| Action | Owner | Timeline | Estimated Effort |
|--------|-------|----------|-----------------|
| Classify all current vendors into tiers | Procurement / Legal | 30 days | 2–3 days internal |
| Complete DPAs for all vendors handling personal data | Legal | 60 days | Legal counsel time |
| Request SOC 2 reports from Critical vendors | Procurement / CISO | 60 days | Minimal |
| Build vendor risk questionnaire template | GRC Analyst | 30 days | 1–2 days internal |
| Implement annual vendor review calendar | GRC Analyst | 30 days | Minimal |

---

## Recommended Decision

> **Leadership is asked to formally adopt a tiered TPRM framework and mandate that all vendors handling customer data have a signed DPA and have been reviewed within the past 12 months.**

This is low-cost, high-impact risk reduction. The primary investment is time approximately 10–15 days of internal effort to stand up the framework initially, and 3–5 days per year to maintain it.

Failure to take action leaves FinTech Co exposed to regulatory, legal, and reputational consequences that are disproportionate to the cost of prevention.

---

## Next Steps

| Action | Owner | Timeline |
|--------|-------|----------|
| Present TPRM framework proposal to leadership | GRC Analyst | 2 weeks |
| Legal review of existing DPA coverage | Head of Legal | 4 weeks |
| Vendor tier classification completed | Procurement | 4 weeks |
| SOC 2 requests sent to Critical vendors | CISO | 6 weeks |

---

*This brief was prepared by the GRC function for senior leadership. A full vendor inventory and TPRM policy draft are available on request.*

---

*This document is a portfolio artefact created for a fictional fintech organisation (FinTech Co, 50 employees). All figures and scenarios are illustrative and reflect real-world GRC communication methodology.*
