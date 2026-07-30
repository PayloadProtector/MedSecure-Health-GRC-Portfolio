# MedSecure Health — Risk Treatment Plan

**Milestone 3, Deliverable 2** | GRC Portfolio Project
**Document Owner:** GRC Function / CISO
**Version:** 1.0
**Effective Date:** July 2026

---

## 1. Purpose

This document records MedSecure Health's treatment decision for each risk identified in the Risk Register (Deliverable 06), the specific remediation actions, ownership, timelines, and the resulting residual risk after treatment. Per ISO 27001 Clause 6.1.3, every risk must have a documented treatment decision — leaving a risk untreated without an explicit "accept" decision is itself a finding an auditor will flag.

## 2. Treatment Options

| Option | Meaning |
|---|---|
| **Mitigate** | Reduce likelihood and/or impact through additional controls |
| **Transfer** | Shift financial impact via insurance or contractual risk-shifting (e.g., vendor liability clauses) |
| **Avoid** | Eliminate the risk by discontinuing the activity that creates it |
| **Accept** | Formally acknowledge the risk and take no further action, because cost of treatment exceeds the risk, or residual risk is within appetite |

---

## 3. Treatment Plan

| ID | Risk | Score | Treatment Decision | Remediation Action | Owner | Target Date | Residual Score | Residual Rating |
|---|---|---|---|---|---|---|---|---|
| R-01 | Ransomware attack | 15 (High) | Mitigate | Implement immutable/air-gapped backups; conduct quarterly recovery drills; deploy EDR with ransomware-specific detection rules | Security Ops | 60 days | 6 | Medium |
| R-04 | AWS S3 misconfiguration | 15 (High) | Mitigate | Deploy Cloud Security Posture Management (CSPM) tooling; enforce infrastructure-as-code review gates; block public bucket policies at the org level | Security Ops | 45 days | 5 | Low |
| R-02 | Accidental PHI email disclosure | 12 (High) | Mitigate | Deploy outbound DLP scanning with PHI pattern detection; add "external recipient" warning banners | IT / Security Ops | 60 days | 8 | Medium |
| R-03 | Third-party vendor breach | 12 (High) | Mitigate + Transfer | Tiered vendor risk assessment based on data sensitivity; require cyber liability insurance in vendor contracts; annual BAA compliance attestation | GRC / Legal | 90 days | 8 | Medium |
| R-06 | Credential compromise | 12 (High) | Mitigate | Enforce MFA org-wide (close any remaining gaps); deploy breached-password screening at login | Security Ops | 30 days | 6 | Medium |
| R-07 | Unpatched vulnerability exploited | 12 (High) | Mitigate | Formalize patch SLA (Critical: 72 hrs, High: 14 days); implement automated vulnerability scanning with ticketing integration | Security Ops | 60 days | 6 | Medium |
| R-13 | Phishing/social engineering | 12 (High) | Mitigate | Launch quarterly phishing simulation program; tie repeat-failure to targeted retraining | GRC / HR | 60 days | 8 | Medium |
| R-05 | Insider threat | 8 (Medium) | Mitigate | Implement anomaly-based audit log alerting for unusual PHI access patterns | Security Ops | 90 days | 6 | Medium |
| R-08 | Lost/stolen unencrypted laptop | 8 (Medium) | Mitigate | Verify and enforce full-disk encryption via MDM policy; enable remote wipe capability | IT | 45 days | 4 | Low |
| R-10 | PCI-DSS non-compliance | 8 (Medium) | Mitigate | Complete annual PCI-DSS self-assessment questionnaire (SAQ); remediate any scan findings | GRC / IT | 90 days | 6 | Medium |
| R-11 | Cloud/AWS outage | 9 (Medium) | Accept | Residual risk accepted given multi-AZ architecture already in place; document in BC/DR plan; revisit if SLA breaches occur | CISO | N/A (accepted) | 9 | Medium |
| R-12 | Inadequate offboarding | 9 (Medium) | Mitigate | Automate deprovisioning trigger from HR system directly into identity provider (remove manual step) | IT | 60 days | 4 | Low |
| R-14 | Regulatory change gap | 9 (Medium) | Mitigate | Formalize quarterly regulatory landscape review as a recurring GRC task (already scoped in Deliverable 01) | GRC | Ongoing | 6 | Medium |
| R-09 | Missed breach notification deadline | 10 (Medium) | Mitigate | Build a breach notification checklist/runbook with calendar-based deadline tracking, tied to Incident Response Policy triage step | GRC / Legal | 30 days | 5 | Low |
| R-15 | Insufficient logging | 6 (Medium) | Mitigate | Centralize logging via SIEM; define minimum log retention (align to HIPAA's 6-year documentation retention expectation) | Security Ops | 90 days | 3 | Low |

---

## 4. Treatment Decision Rationale — Notable Cases

**R-11 (AWS outage) — Accept, not Mitigate.**
This is the one risk in the register formally accepted rather than treated further. The rationale: MedSecure already runs a multi-AZ architecture, meaning the marginal cost of additional resilience (e.g., multi-region failover) is disproportionate to the residual risk. This is a realistic and defensible acceptance decision — showing you can accept a risk with clear reasoning is just as important as showing you can mitigate one. A GRC program that treats every single risk signals it doesn't understand cost-benefit tradeoffs.

**R-03 (Vendor breach) — Mitigate + Transfer, combined.**
This shows a risk doesn't have to map to exactly one treatment type. MedSecure both reduces likelihood (via vendor risk assessments) and transfers financial impact (via required cyber liability insurance in contracts) — a common real-world pattern for third-party risk specifically, since you can never fully control a vendor's internal security.

---

## 5. Residual Risk Summary

| Rating | Count Before Treatment | Count After Treatment (Projected) |
|---|---|---|
| Critical | 0 | 0 |
| High | 7 | 0 |
| Medium | 7 | 8 |
| Low | 1 | 7 |

**Observation:** treatment brings every High-rated risk down to Medium or Low — none are eliminated to zero, which is realistic. Risk treatment reduces risk to an acceptable level; it doesn't eliminate it entirely. This is a distinction worth being able to articulate clearly: a portfolio that shows every risk driven to "Low" looks unrealistic to anyone who's actually done this work.

---

## Next Step

Milestone 3 is now complete: Risk Register → Risk Treatment Plan. Milestone 4 begins with the **NIST 800-53 Gap Analysis** — selecting a control baseline and scoring MedSecure Health's current maturity against it, building directly on the treatment actions defined above.
