# MedSecure Health — Information Security Policy

**Milestone 1, Deliverable 2** | GRC Portfolio Project
**Document Owner:** Chief Information Security Officer (CISO)
**Approved By:** Executive Leadership / Board of Directors
**Version:** 1.0
**Effective Date:** July 2026
**Review Cycle:** Annual, or upon material change to business, technology, or regulatory environment

---

## 1. Purpose

This policy establishes MedSecure Health's commitment to protecting the confidentiality, integrity, and availability (CIA) of its information assets — including Protected Health Information (PHI), payment card data, and business-critical systems — in compliance with applicable law and in alignment with recognized international standards.

This policy is the top-level governance document of MedSecure Health's Information Security Management System (ISMS) and sits above all subordinate security policies, standards, and procedures.

## 2. Scope

This policy applies to:

- All employees, contractors, interns, and third parties with access to MedSecure Health systems or data
- All information assets owned, leased, or managed by MedSecure Health, including cloud infrastructure (AWS), applications, endpoints, and physical facilities
- All data classifications, with particular emphasis on PHI and cardholder data (CHD) given regulatory exposure identified in the Regulatory Landscape Map (Deliverable 01)

This policy does **not** cover data or systems outside MedSecure Health's operational control (e.g., patient personal devices), though related expectations are addressed in the Acceptable Use Policy.

## 3. Policy Statement

MedSecure Health is committed to:

1. Protecting the confidentiality, integrity, and availability of PHI and other sensitive data in accordance with the HIPAA Security Rule (45 CFR §164.308–318) and other applicable regulations identified in Deliverable 01
2. Implementing and maintaining an Information Security Management System (ISMS) aligned with **ISO/IEC 27001**
3. Applying control depth informed by **NIST SP 800-53** (Moderate baseline) where additional technical rigor is warranted
4. Conducting regular risk assessments and ensuring risk treatment decisions are documented, owned, and reviewed
5. Ensuring every employee and contractor understands their role in protecting information assets
6. Reporting, investigating, and learning from security incidents in a timely and transparent manner
7. Continually improving the ISMS through management review, audit findings, and evolving threat and regulatory landscapes

## 4. Roles & Responsibilities

| Role | Responsibility |
|---|---|
| **Board of Directors / Executive Leadership** | Ultimate accountability for the security program; approves policy and risk appetite |
| **Chief Information Security Officer (CISO)** | Owns the ISMS; reports program status and material risks to leadership; approves exceptions |
| **IT/Security Operations** | Implements technical controls; monitors systems; responds to incidents |
| **Compliance/GRC Function** | Maintains regulatory mapping, conducts internal audits, tracks remediation |
| **People Managers** | Ensure their teams complete required training and follow policy |
| **All Workforce Members** | Comply with this policy and report suspected incidents or violations |
| **Third-Party Vendors/Business Associates** | Comply with contractual security requirements (see Vendor Management Policy) and applicable Business Associate Agreements (BAAs) under HIPAA |

## 5. Information Security Objectives

MedSecure Health's security program is built around the following measurable objectives, reviewed annually as part of management review:

- Maintain zero substantiated HIPAA breach findings resulting from control failure
- Complete an annual risk assessment covering 100% of in-scope systems handling PHI or CHD
- Achieve and maintain ISO 27001 certification readiness
- Ensure 100% of workforce members complete annual security awareness training
- Maintain incident response capability with a target of initial triage within 4 hours of detection

## 6. Governing Sub-Policies

This policy establishes the umbrella under which the following subordinate policies operate (developed in later milestones of this project):

| Sub-Policy | Primary Regulatory/Framework Driver |
|---|---|
| Access Control Policy | HIPAA Security Rule §164.312(a); ISO 27001 Annex A.5, A.8 |
| Risk Management Policy | ISO 27001 Clause 6.1; NIST SP 800-30 |
| Incident Response Policy | HIPAA Breach Notification Rule; ISO 27001 Annex A.5.24-28 |
| Acceptable Use Policy | Internal governance; supports FTC Act Section 5 obligations |
| Vendor/Third-Party Risk Management Policy | HIPAA Business Associate requirements; ISO 27001 Annex A.5.19-22 |
| Data Classification & Handling Policy | HIPAA Privacy Rule; PCI-DSS Requirement 3 |

## 7. Compliance & Enforcement

- Violations of this policy may result in disciplinary action up to and including termination, consistent with HR policy
- Violations involving PHI may additionally trigger obligations under the HIPAA Breach Notification Rule, including mandatory reporting timelines
- Contracted third parties found in violation of security requirements are subject to remedies defined in their governing agreements, including BAA termination where applicable

## 8. Exceptions

Any deviation from this policy must be:

1. Documented with business justification
2. Risk-assessed by the CISO or delegate
3. Time-bound with a defined review/expiration date
4. Formally approved before implementation

Undocumented exceptions are treated as policy violations.

## 9. Review & Continual Improvement

This policy is reviewed at minimum annually, and additionally upon:

- Material changes to MedSecure Health's business model, data types, or geographic footprint (see Regulatory Landscape Map watch-list triggers)
- Significant security incidents
- Changes to applicable law or regulation
- Findings from internal or external audits

## 10. Definitions

| Term | Definition |
|---|---|
| **PHI** | Protected Health Information as defined under HIPAA, 45 CFR §160.103 |
| **ISMS** | Information Security Management System, per ISO/IEC 27001 |
| **CHD** | Cardholder Data, as defined under PCI-DSS |
| **BAA** | Business Associate Agreement, a required contract under HIPAA when a third party handles PHI on a covered entity's behalf |

---

## Traceability Note (for portfolio/interview use)

This policy deliberately references specific HIPAA citations (e.g., §164.308) and specific ISO 27001 clauses/Annex A control numbers rather than vague statements like "we comply with HIPAA." This is a distinguishing trait of a well-written policy — an auditor or interviewer can trace every commitment back to a specific legal or framework requirement, which is exactly what the Regulatory Landscape Map (Deliverable 01) was built to support.

## Next Step

This policy feeds directly into **Milestone 2: ISMS per ISO 27001**, starting with the **Scope Statement and Statement of Applicability (SoA)** — the document that determines which of ISO 27001's Annex A controls apply to MedSecure Health and why.
