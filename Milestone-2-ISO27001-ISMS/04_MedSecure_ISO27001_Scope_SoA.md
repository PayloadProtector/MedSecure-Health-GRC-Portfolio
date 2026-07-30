# MedSecure Health — ISO 27001 Scope Statement & Statement of Applicability (SoA)

**Milestone 2, Deliverable 1** | GRC Portfolio Project
**Document Owner:** CISO / GRC Function
**Version:** 1.0
**Effective Date:** July 2026

---

## 1. Purpose

This document defines the boundaries of MedSecure Health's Information Security Management System (ISMS) under ISO/IEC 27001, and records which Annex A controls are applicable, with justification for inclusion or exclusion. This is one of the most important artifacts in an ISO 27001 program — it is the document an external certification auditor reviews first.

---

## 2. ISMS Scope Statement

The ISMS covers all people, processes, and technology involved in the collection, storage, processing, and transmission of Protected Health Information (PHI) and payment card data (CHD) in support of MedSecure Health's patient portal, telehealth platform, and insurance claims processing services.

**In scope:**
- Production AWS cloud environment hosting the patient portal, telehealth, and claims processing applications
- Corporate IT environment (employee laptops, internal network, email, identity systems)
- Physical offices used by workforce members with access to in-scope systems
- Third-party vendors and business associates with access to PHI or CHD

**Out of scope:**
- Marketing website and blog (no PHI or CHD processed)
- Any future EU operations (not yet established; would trigger scope reassessment)

**Interfaces and dependencies:** AWS as a cloud service provider is included via a shared responsibility model; MedSecure Health is accountable for application-layer and configuration controls, while AWS's own ISO 27001 and SOC 2 certifications cover the underlying physical and infrastructure layer.

---

## 3. Statement of Applicability (SoA) — Summary by Control Category

ISO/IEC 27001:2022 Annex A organizes controls into four themes: Organizational, People, Physical, and Technological. Below is a representative sample across each theme (a full SoA would address all 93 Annex A controls; this sample demonstrates the methodology and covers the controls most material to MedSecure Health's risk profile).

| Control ID | Control Name | Applicable? | Justification |
|---|---|---|---|
| A.5.1 | Policies for information security | Yes | Directly implemented via the Information Security Policy (Deliverable 02) |
| A.5.7 | Threat intelligence | Yes | Healthcare sector is a high-value target; threat intel feeds inform risk assessment |
| A.5.19 | Information security in supplier relationships | Yes | Required given AWS hosting and multiple vendors handling PHI |
| A.5.23 | Information security for use of cloud services | Yes | Core to MedSecure's AWS-based architecture |
| A.5.24 | Incident management planning | Yes | Required for HIPAA Breach Notification Rule compliance |
| A.5.31 | Legal, statutory, regulatory, and contractual requirements | Yes | Directly maps to the Regulatory Landscape Map (Deliverable 01) |
| A.6.3 | Information security awareness, education, and training | Yes | Annual training is a stated objective in the Information Security Policy |
| A.6.6 | Confidentiality or non-disclosure agreements | Yes | Required for all workforce and contractors given PHI exposure |
| A.7.1 | Physical security perimeters | Yes | Applies to corporate offices; data center perimeter covered by AWS's own certification |
| A.7.4 | Physical security monitoring | Partial | Applies to corporate offices only; not applicable to AWS data centers (covered under shared responsibility) |
| A.8.1 | User endpoint devices | Yes | Applies to all workforce laptops accessing in-scope systems |
| A.8.8 | Management of technical vulnerabilities | Yes | Core to protecting PHI-handling applications; supports PCI-DSS scanning requirements |
| A.8.16 | Monitoring activities | Yes | Required for both HIPAA audit control requirements and incident detection |
| A.8.24 | Use of cryptography | Yes | Required for PHI encryption at rest and in transit (HIPAA Security Rule addressable/required specifications) |
| A.8.28 | Secure coding | Yes | Applies given MedSecure develops its own patient-facing applications |
| A.5.29 | Information security during disruption | Yes | Supports business continuity objective in Information Security Policy |
| A.7.10 | Storage media | Excluded | MedSecure Health uses cloud-native storage exclusively; no physical removable media in the in-scope environment |
| A.8.30 | Outsourced development | Excluded | All application development is performed in-house; no outsourced development currently in scope |

*(Note: a complete SoA for a real certification effort would document a justification for all 93 controls, not a sample. This document demonstrates the reasoning method — the same approach shown above would be applied systematically to every remaining control.)*

---

## 4. Key Exclusions and Rationale

Exclusions are just as important to document as inclusions, since an auditor will specifically probe why a control was excluded.

| Excluded Control | Rationale |
|---|---|
| A.7.10 (Storage media) | No physical removable media handling PHI exists in the in-scope environment; all storage is cloud-native |
| A.8.30 (Outsourced development) | Development is fully in-house; this control would become applicable if MedSecure contracts external developers |

---

## 5. Traceability Back to Regulatory and Risk Drivers

Every applicable control above should ultimately trace back to either a legal requirement (from Deliverable 01) or a risk identified during risk assessment (Milestone 3). This traceability is what makes an SoA defensible rather than a generic checklist copy-paste.

---

## Next Step

With the ISMS scope and SoA established, Milestone 2 continues with the ISMS policy set (access control, incident response, acceptable use) and the management review process, before moving into Milestone 3: Risk Management.
