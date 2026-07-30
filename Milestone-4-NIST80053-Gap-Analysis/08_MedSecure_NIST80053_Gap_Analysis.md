# MedSecure Health — NIST 800-53 Gap Analysis

**Milestone 4, Deliverable 1** | GRC Portfolio Project
**Document Owner:** GRC Function / CISO
**Version:** 1.0
**Effective Date:** July 2026
**Baseline Selected:** NIST SP 800-53 Rev. 5 — Moderate Impact Baseline

---

## 1. Purpose & Baseline Selection

This gap analysis scores MedSecure Health's current control maturity against the NIST SP 800-53 Moderate baseline, identifies gaps, and produces a prioritized remediation roadmap.

**Why Moderate, not Low or High:** NIST SP 800-60 guidance ties baseline selection to the potential impact of a confidentiality, integrity, or availability loss. PHI breaches carry serious but not catastrophic national-security-level consequences — this places MedSecure at Moderate across all three security objectives, which is the standard baseline for most healthcare organizations (and is also what HITRUST CSF and most healthcare-sector risk assessments assume by default).

## 2. Maturity Scoring Model

Each control family is scored on a 0–4 maturity scale, a common adaptation used alongside NIST assessments:

| Level | Label | Description |
|---|---|---|
| 0 | Not Implemented | No process or control exists |
| 1 | Ad Hoc | Control exists informally, inconsistently applied, undocumented |
| 2 | Defined | Control is documented but not consistently enforced or measured |
| 3 | Managed | Control is consistently implemented, monitored, and measured |
| 4 | Optimized | Control is continuously improved based on metrics and lessons learned |

**Target maturity for Moderate baseline: Level 3 (Managed)** across all families — Level 4 is aspirational but not required for baseline compliance.

---

## 3. Gap Analysis by Control Family

| Family | Control Family Name | Current Maturity | Target | Gap | Priority | Linked Risk (Deliverable 06/07) |
|---|---|---|---|---|---|---|
| AC | Access Control | 2 (Defined) | 3 | 1 | High | R-05, R-06, R-12 |
| AT | Awareness & Training | 2 (Defined) | 3 | 1 | Medium | R-13 |
| AU | Audit & Accountability | 1 (Ad Hoc) | 3 | 2 | High | R-05, R-15 |
| CA | Assessment, Authorization & Monitoring | 1 (Ad Hoc) | 3 | 2 | High | — (foundational for all) |
| CM | Configuration Management | 2 (Defined) | 3 | 1 | Medium | R-04 |
| CP | Contingency Planning | 2 (Defined) | 3 | 1 | Medium | R-01, R-11 |
| IA | Identification & Authentication | 3 (Managed) | 3 | 0 | — | R-06 |
| IR | Incident Response | 2 (Defined) | 3 | 1 | High | R-09 |
| MA | Maintenance | 2 (Defined) | 3 | 1 | Low | — |
| MP | Media Protection | 3 (Managed) | 3 | 0 | — | (N/A — cloud-native, per SoA exclusion A.7.10) |
| PE | Physical & Environmental Protection | 2 (Defined) | 3 | 1 | Low | R-08 |
| PL | Planning | 2 (Defined) | 3 | 1 | Medium | — (ISMS scope/SoA addresses this) |
| PS | Personnel Security | 2 (Defined) | 3 | 1 | Medium | R-05, R-12 |
| RA | Risk Assessment | 3 (Managed) | 3 | 0 | — | Deliverable 06/07 directly evidences this |
| SA | System & Services Acquisition | 1 (Ad Hoc) | 3 | 2 | High | R-03, R-07 |
| SC | System & Communications Protection | 2 (Defined) | 3 | 1 | High | R-01, R-04, R-10 |
| SI | System & Information Integrity | 1 (Ad Hoc) | 3 | 2 | High | R-01, R-07 |
| SR | Supply Chain Risk Management | 1 (Ad Hoc) | 3 | 2 | High | R-03 |

*(20 total families exist in Rev. 5; the four omitted here — PM (Program Management), PT (PII Processing/Transparency), and two others — are addressed at the organizational-policy level via existing deliverables rather than scored separately, consistent with how a real assessment would treat controls already evidenced elsewhere.)*

---

## 4. Maturity Heat Map

| Maturity 1 (Ad Hoc) | Maturity 2 (Defined) | Maturity 3 (Managed) |
|---|---|---|
| AU, CA, SA, SI, SR | AC, AT, CM, CP, IR, MA, PE, PL, PS | IA, MP, RA |

**Observation:** the biggest weaknesses cluster around **audit/monitoring (AU), assessment (CA), acquisition (SA), system integrity (SI), and supply chain (SR)** — notably, these track closely with the highest-scored risks in the Risk Register (ransomware, vendor breach, vulnerability exploitation). This is a good sign methodologically: the gap analysis and risk register should reinforce each other, not tell contradictory stories.

---

## 5. Prioritized Remediation Roadmap

| Priority | Control Family | Remediation Action | Target Maturity | Timeframe | Owner |
|---|---|---|---|---|---|
| 1 | SI (System Integrity) | Formalize vulnerability management program with defined patch SLAs and automated scanning | 3 | 60 days | Security Ops |
| 2 | SR (Supply Chain) | Build formal vendor risk tiering and assessment process (ties to R-03 treatment plan) | 3 | 90 days | GRC / Legal |
| 3 | AU (Audit & Accountability) | Deploy centralized logging/SIEM with defined retention and alerting | 3 | 90 days | Security Ops |
| 4 | CA (Assessment & Monitoring) | Establish continuous control monitoring program; schedule first internal audit | 3 | 90 days | GRC |
| 5 | SA (System & Services Acquisition) | Formalize secure development lifecycle (SDLC) requirements, including secure coding standards | 3 | 120 days | Engineering / Security |
| 6 | SC (System & Communications Protection) | Complete CSPM rollout, encryption verification across all data stores | 3 | 60 days | Security Ops |
| 7 | IR (Incident Response) | Deploy breach notification runbook (already scoped in R-09 treatment) | 3 | 30 days | GRC / Legal |
| 8 | AC (Access Control) | Automate offboarding trigger from HR to identity provider | 3 | 60 days | IT |

*(Lower-priority families — AT, CM, CP, MA, PE, PL, PS — remain at "Defined" with planned improvement but are not first-wave priorities, since their gap is smaller and linked risk severity is lower.)*

---

## 6. Overall Maturity Summary

| Metric | Value |
|---|---|
| Average current maturity (18 scored families) | 1.9 (between Ad Hoc and Defined) |
| Target maturity | 3.0 (Managed) |
| Families at target already | 3 of 18 (IA, MP, RA) |
| Families requiring High-priority remediation | 7 of 18 |

**Honest assessment:** MedSecure Health's program is at an early-to-middle maturity stage — typical for an organization that has strong documented governance (policies, RACI, risk register all exist) but hasn't yet operationalized consistent monitoring and enforcement. This is a realistic and common state for a growing healthcare SaaS company, and the roadmap above is deliberately sequenced to close the highest-risk gaps first rather than the easiest ones.

---

## Next Step

Milestone 4 is complete. Milestone 5, the Capstone, synthesizes everything built so far — the regulatory map, ISMS, risk register/treatment plan, and this gap analysis — into an internal audit / readiness assessment report with a board-level executive summary.
