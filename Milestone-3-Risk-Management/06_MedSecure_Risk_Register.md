# MedSecure Health — Risk Register

**Milestone 3, Deliverable 1** | GRC Portfolio Project
**Document Owner:** GRC Function
**Version:** 1.0
**Effective Date:** July 2026
**Methodology:** Qualitative risk scoring adapted from NIST SP 800-30 (Guide for Conducting Risk Assessments)

---

## 1. Methodology

Each risk is scored on two dimensions:

- **Likelihood (1–5):** probability the risk event occurs within the next 12 months
- **Impact (1–5):** severity of harm if it occurs — considering data exposure, financial cost, regulatory penalty, and reputational damage

**Risk Score = Likelihood × Impact** (range 1–25)

| Score Range | Rating | Response Expectation |
|---|---|---|
| 20–25 | Critical | Immediate treatment required; escalate to executive leadership |
| 12–19 | High | Treatment plan required within 30 days |
| 6–11 | Medium | Treatment plan required within 90 days |
| 1–5 | Low | Monitor; accept or treat opportunistically |

**Likelihood scale:** 1 = Rare (unlikely in next 12 months) → 5 = Almost certain (expected to occur)
**Impact scale:** 1 = Negligible → 5 = Severe (major breach, regulatory action, business-threatening)

---

## 2. Risk Register

| ID | Risk Description | Category | Likelihood | Impact | Score | Rating | Existing Controls | Mapped Control (SoA) |
|---|---|---|---|---|---|---|---|---|
| R-01 | Ransomware attack encrypts production systems handling PHI | Cyber/Technical | 3 | 5 | 15 | High | Endpoint detection, backups, network segmentation | A.8.8, A.8.16 |
| R-02 | Employee accidentally emails PHI to wrong recipient or personal account | Human/Operational | 4 | 3 | 12 | High | Acceptable Use Policy, DLP tooling (partial) | Acceptable Use Policy |
| R-03 | Third-party vendor with PHI access suffers its own breach | Third-Party | 3 | 4 | 12 | High | Vendor risk assessment, BAAs | A.5.19, A.5.23 |
| R-04 | Misconfigured AWS S3 bucket exposes PHI publicly | Cloud/Technical | 3 | 5 | 15 | High | Cloud security posture monitoring (assumed partial) | A.5.23, A.8.16 |
| R-05 | Insider threat — employee misuses legitimate access to PHI | Human/Insider | 2 | 4 | 8 | Medium | Access reviews, audit logging | A.8.16, Access Control Policy |
| R-06 | Weak/reused credentials lead to account compromise | Cyber/Technical | 4 | 3 | 12 | High | MFA requirement (Access Control Policy) | A.8.1, Access Control Policy |
| R-07 | Unpatched vulnerability in patient portal exploited | Cyber/Technical | 3 | 4 | 12 | High | Vulnerability management program | A.8.8 |
| R-08 | Loss/theft of an unencrypted employee laptop containing PHI | Physical/Technical | 2 | 4 | 8 | Medium | Full-disk encryption (assumed), device lock policy | A.8.1, A.8.24 |
| R-09 | Failure to meet 60-day HIPAA breach notification deadline | Compliance/Process | 2 | 5 | 10 | Medium | Incident Response Policy with defined triage SLA | A.5.24-28 |
| R-10 | Payment card data exposure due to PCI-DSS non-compliance | Compliance/Cyber | 2 | 4 | 8 | Medium | PCI-DSS scanning (assumed in place) | A.8.24 |
| R-11 | Cloud service (AWS) outage disrupts platform availability | Availability/Third-Party | 3 | 3 | 9 | Medium | Multi-AZ architecture (assumed), BC/DR plan | A.5.29 |
| R-12 | Inadequate offboarding leaves former employee with active access | Human/Process | 3 | 3 | 9 | Medium | Access deprovisioning SLA (24 hrs) | Access Control Policy |
| R-13 | Social engineering/phishing attack targets workforce | Human/Cyber | 4 | 3 | 12 | High | Security awareness training | A.6.3 |
| R-14 | Regulatory change (e.g., new state health privacy law) creates compliance gap | Regulatory/Strategic | 3 | 3 | 9 | Medium | Regulatory landscape monitoring | A.5.31 |
| R-15 | Insufficient logging prevents effective incident investigation | Technical/Process | 2 | 3 | 6 | Medium | Centralized logging (assumed partial) | A.8.16 |

---

## 3. Risk Heat Map Summary

| | Impact: Low (1-2) | Impact: Medium (3) | Impact: High (4-5) |
|---|---|---|---|
| **Likelihood: High (4-5)** | — | R-06, R-13 | R-01, R-04 |
| **Likelihood: Medium (3)** | — | R-11, R-12, R-14 | R-03, R-07 |
| **Likelihood: Low (1-2)** | — | R-15 | R-05, R-08, R-09, R-10 |

**Observation:** R-01 (ransomware) and R-04 (cloud misconfiguration) sit in the highest-severity quadrant and should be prioritized for treatment first — this is exactly the kind of prioritization logic a hiring manager wants to see, not just a flat list.

---

## 4. Top 5 Risks Requiring Immediate Attention

1. **R-01 — Ransomware** (Score 15): Highest combined severity given healthcare's status as a top ransomware target sector; recommend prioritizing immutable backups and tested recovery procedures
2. **R-04 — Cloud misconfiguration** (Score 15): Cloud misconfigurations are consistently among the top causes of healthcare breaches industry-wide; recommend automated cloud security posture management (CSPM) tooling
3. **R-02 — Accidental PHI disclosure** (Score 12): High likelihood given human error rates; recommend stronger DLP tooling and outbound email scanning
4. **R-03 — Third-party vendor breach** (Score 12): MedSecure's own controls don't protect against a vendor's failure; recommend tiered vendor risk assessment based on data access level
5. **R-13 — Phishing/social engineering** (Score 12): Highest-likelihood item on the list; recommend phishing simulation program in addition to annual training

---

## 5. Notes on Methodology & Limitations

- Likelihood scores are illustrative for portfolio purposes, informed by general industry breach data (e.g., healthcare sector ransomware trends) rather than MedSecure-specific incident history, since MedSecure is fictional
- A real risk register would be built with input from technical teams (to verify what controls actually exist vs. "assumed") and updated at least quarterly
- Several "existing controls" are marked "(assumed)" or "(partial)" — in a real assessment, this is exactly what a control effectiveness testing exercise (Milestone 4) would verify rather than take on faith

---

## Next Step

With the Risk Register built, Milestone 3 continues with the **Risk Treatment Plan** — documenting specific treatment decisions (mitigate, transfer, accept, avoid) and remediation actions for each risk above Medium severity.
