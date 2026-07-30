# MedSecure Health — Information Security & Compliance Readiness Assessment

**Milestone 5: Capstone Deliverable** | GRC Portfolio Project
**Report Type:** Internal Audit / ISO 27001 & HIPAA Readiness Assessment
**Prepared for:** Board of Directors and Executive Leadership
**Prepared by:** GRC Function
**Date:** July 2026
**Classification:** Internal — Confidential

---

## Executive Summary

MedSecure Health has spent the past two quarters building a formal Governance, Risk, and Compliance (GRC) program in response to its growing regulatory exposure as a healthcare technology company handling Protected Health Information (PHI) for approximately 50,000 patients. This report summarizes the current state of that program, our overall readiness for ISO 27001 certification and continued HIPAA compliance, and the priority actions leadership should expect to fund and support over the next two quarters.

**Bottom line:** MedSecure Health has established strong governance foundations — clear policy, defined accountability, and a documented risk picture — but has not yet fully operationalized the monitoring and enforcement layer that turns those foundations into a mature, auditable security program. This is a normal and expected stage for a company at our size and growth trajectory. It is not a crisis; it is a roadmap.

**Key findings:**

- Governance structure (policy, roles, accountability) is in place and well-documented
- 15 material risks have been identified and scored; none rated Critical, though 7 are rated High and require active remediation
- Against the NIST 800-53 Moderate baseline, MedSecure Health scores an average maturity of 1.9 out of 4 (between "Ad Hoc" and "Defined"), with the most significant gaps in audit logging, vendor risk management, and secure software acquisition
- The two highest-severity risks — ransomware and cloud misconfiguration — are also the two areas where remediation investment will have the greatest risk-reduction impact
- No findings in this assessment indicate an active compliance violation; findings reflect program maturity gaps, not current legal non-compliance

**Recommended executive action:** Approve budget and staffing for the eight-item remediation roadmap (Section 5), prioritizing vulnerability management and vendor risk processes within the next 60–90 days.

---

## 1. Purpose & Scope

This assessment evaluates MedSecure Health's information security governance, risk management, and compliance posture against three reference points:

1. **Legal/regulatory obligations** — primarily HIPAA (Privacy Rule, Security Rule, Breach Notification Rule), with PCI-DSS as a secondary contractual obligation
2. **ISO/IEC 27001** — as MedSecure's chosen ISMS framework
3. **NIST SP 800-53 (Moderate baseline)** — as the technical control depth reference

**In scope:** the production AWS environment (patient portal, telehealth, claims processing), corporate IT, physical offices, and third-party vendors with PHI access — consistent with the ISMS Scope Statement.

**Out of scope:** marketing website, any future EU operations (per Regulatory Landscape Map watch list).

## 2. Methodology

This assessment synthesizes four prior work products, each independently developed and cross-referenced:

| Source Document | Contribution to This Assessment |
|---|---|
| Regulatory Landscape Map | Defines the legal obligations this program must satisfy |
| Information Security Policy, ISMS Policy Set, RACI Matrix | Evidences governance structure and accountability |
| ISO 27001 Scope Statement & SoA | Defines ISMS boundaries and control applicability |
| Risk Register & Risk Treatment Plan | Provides the risk-based prioritization lens |
| NIST 800-53 Gap Analysis | Provides the technical maturity scoring |

## 3. Governance Posture Summary

MedSecure Health's governance layer is its strongest asset going into an ISO 27001 certification effort:

- A board-approved Information Security Policy establishes clear commitments tied to specific legal citations (not generic language)
- A RACI matrix defines ownership across 20+ core GRC activities, with intentional design choices (e.g., Legal — not the CISO — holds accountability for regulatory breach reporting decisions)
- Sub-policies for Access Control, Incident Response, and Acceptable Use are documented and mapped to specific Annex A controls and HIPAA citations
- A quarterly Management Review process is defined per ISO 27001 Clause 9.3, ensuring the ISMS remains a living system rather than a static document set

**Assessment:** Governance maturity is assessed as **adequate for certification readiness**, pending evidence that the Management Review process has actually convened on schedule (this assessment evaluates documented process design, not yet operational history, since the program is newly established).

## 4. Risk Management Summary

Fifteen risks were formally assessed using a Likelihood × Impact methodology adapted from NIST SP 800-30:

- **0 Critical, 7 High, 7 Medium, 1 Low** (pre-treatment)
- Following the documented Risk Treatment Plan, projected residual risk shows **0 High-rated risks remaining**, with the distribution shifting to 8 Medium and 7 Low
- One risk (R-11, AWS regional outage) was formally **accepted** rather than further mitigated, with documented rationale — this is a positive maturity indicator, showing risk decisions are deliberate rather than reflexively over-engineered

**Assessment:** Risk management process is assessed as **methodologically sound**. The primary gap is operational: treatment actions are planned but implementation status has not yet been independently verified (a task for the next internal audit cycle, once remediation timelines in Section 5 elapse).

## 5. Technical Control Maturity Summary (NIST 800-53)

Against the Moderate baseline, MedSecure Health's average control family maturity is **1.9 out of 4** ("Ad Hoc" to "Defined"). Three families (Identification & Authentication, Media Protection, Risk Assessment) already meet the "Managed" target; the remaining fifteen require continued investment.

**The five highest-priority gaps**, in order of remediation priority:

1. System & Information Integrity (vulnerability/patch management)
2. Supply Chain Risk Management (vendor risk process)
3. Audit & Accountability (centralized logging/monitoring)
4. Assessment, Authorization & Monitoring (continuous control monitoring, internal audit cadence)
5. System & Services Acquisition (secure development lifecycle)

Notably, these gaps correlate directly with the highest-scored risks in Section 4 (ransomware, vendor breach, vulnerability exploitation) — indicating the risk assessment and technical gap analysis are internally consistent, which strengthens confidence in both.

**Assessment:** Technical control maturity is assessed as **developing**, consistent with an organization that has prioritized governance and policy work first (a defensible sequencing choice) but must now invest in operational enforcement to reach ISO 27001 certification readiness or a clean SOC 2 Type II opinion.

## 6. Overall Program Rating

| Dimension | Rating | Basis |
|---|---|---|
| Governance & Policy | Adequate | Sections 3 |
| Risk Management Process | Sound | Section 4 |
| Technical Control Maturity | Developing | Section 5 |
| **Overall Program Readiness** | **Developing — On Track** | Composite of above |

This is not a failing assessment. It reflects a program in an active, well-sequenced build phase, with the hardest-to-fake element — governance and risk-based thinking — already in solid shape.

## 7. Recommendations & Roadmap

The eight-item remediation roadmap from the NIST 800-53 Gap Analysis (Deliverable 08) is adopted as this assessment's formal recommendation set, with the following executive framing:

| Priority | Action | Investment Needed | Timeframe |
|---|---|---|---|
| 1 | Vulnerability management program (patch SLAs, automated scanning) | Tooling + Security Ops time | 60 days |
| 2 | Vendor risk tiering & assessment process | GRC/Legal time; possible tooling | 90 days |
| 3 | Centralized logging/SIEM | Tooling budget | 90 days |
| 4 | Continuous control monitoring + first internal audit | GRC time; possible external auditor engagement | 90 days |
| 5 | Secure development lifecycle formalization | Engineering + Security time | 120 days |

**Budget consideration for leadership:** items 1, 3, and 5 likely require new tooling spend; items 2 and 4 are primarily process and staffing investments. A detailed cost estimate should be developed by IT/Security leadership as a follow-on to this report.

## 8. Conclusion

MedSecure Health has built the governance and risk-management foundation expected of a maturing healthcare technology company handling sensitive patient data. The path to ISO 27001 certification readiness and continued HIPAA/PCI-DSS compliance is clear, specific, and achievable within approximately two to three quarters, contingent on executing the roadmap above. No findings in this assessment indicate current non-compliance requiring immediate escalation beyond normal remediation planning.

---

## Appendix: Portfolio Note

This capstone report — and the eight supporting deliverables that feed it (Regulatory Landscape Map, Information Security Policy, RACI Matrix, ISO 27001 Scope/SoA, ISMS Policy Set, Risk Register, Risk Treatment Plan, NIST 800-53 Gap Analysis) — together demonstrate the full GRC lifecycle: understanding *why* regulation matters, translating law into policy, assessing and treating risk, measuring technical maturity against a recognized standard, and synthesizing all of it into a decision-ready report for leadership. This is the complete arc most GRC analyst and associate roles expect a candidate to be able to walk through in an interview.
