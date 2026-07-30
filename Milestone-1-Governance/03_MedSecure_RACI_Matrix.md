# MedSecure Health — GRC RACI Matrix

**Milestone 1, Deliverable 3** | GRC Portfolio Project
**Document Owner:** CISO / GRC Function
**Version:** 1.0
**Effective Date:** July 2026

---

## 1. Purpose

This RACI matrix defines who is **Responsible**, **Accountable**, **Consulted**, and **Informed** for the core governance, risk, and compliance activities at MedSecure Health. It operationalizes the roles defined in the Information Security Policy (Deliverable 02) into concrete process ownership.

**Legend:**

| Letter | Meaning |
|---|---|
| **R** | Responsible — does the work |
| **A** | Accountable — owns the outcome, signs off (only one A per activity) |
| **C** | Consulted — provides input before/during the activity (two-way communication) |
| **I** | Informed — kept updated on progress/outcome (one-way communication) |

---

## 2. RACI Matrix

| Activity | Board / Exec Leadership | CISO | Security Ops (IT) | GRC / Compliance | Legal | HR / People Managers | All Workforce | Third-Party Vendors |
|---|---|---|---|---|---|---|---|---|
| Approve Information Security Policy | **A** | R | I | C | C | I | I | — |
| Set risk appetite / tolerance | **A** | R | I | C | C | — | — | — |
| Conduct annual risk assessment | I | **A** | C | R | — | — | — | — |
| Approve risk treatment decisions | I | **A** | R | C | C | — | — | — |
| Maintain risk register | I | A | C | **R** | — | — | — | — |
| Maintain ISO 27001 Statement of Applicability (SoA) | I | **A** | C | R | — | — | — | — |
| Implement technical security controls | I | A | **R** | C | — | — | — | C |
| Conduct internal audit | I | I | C | **R** | — | — | — | — |
| Approve policy exceptions | I | **A** | C | R | C | — | — | — |
| Incident detection & triage | I | A | **R** | C | — | — | I | I |
| Incident response coordination | I | **A** | R | R | C | I | I | I |
| HIPAA breach notification decision | I | **A** | C | R | R | — | — | — |
| Regulatory reporting (e.g., HHS, state AG) | I | A | I | R | **A** | — | — | — |
| Vendor / Business Associate risk assessment | I | A | C | **R** | C | — | — | C |
| Execute Business Associate Agreements (BAAs) | I | C | — | C | **A** | — | — | R |
| Security awareness training delivery | I | A | C | **R** | — | R | I | — |
| Track training completion | I | I | — | **R** | — | R | I | — |
| Access provisioning / deprovisioning | I | A | **R** | C | — | R | I | — |
| Access rights review (periodic) | I | A | C | **R** | — | C | — | — |
| Data classification | I | A | C | **R** | C | — | R | — |
| Physical security controls | I | **A** | R | C | — | — | I | — |
| Business continuity / DR planning | **A** | R | R | C | C | I | I | C |
| Management review of ISMS | **A** | R | I | R | I | I | — | — |
| Report security posture to Board | **A**/I | **R** | — | C | — | — | — | — |

*(Note: "Report security posture to Board" shows the Board as both informed recipient and ultimate accountable party for governance oversight — this dual notation is intentional and worth explaining if asked: the Board is accountable for oversight, while the CISO is responsible for producing and delivering the report.)*

---

## 3. Design Notes (for portfolio/interview use)

A few deliberate choices in this matrix, worth being able to explain:

- **Only one "A" per row.** This is the most common RACI mistake — assigning shared accountability. Even where multiple people are heavily involved (e.g., incident response), exactly one role is ultimately accountable for the outcome.
- **Legal is Accountable for regulatory reporting, not the CISO.** This reflects reality: breach notification to HHS/state AGs is often a legal determination (timing, content, whether a reportable breach occurred), even though Security/GRC does the investigative legwork.
- **Third-party vendors appear as R, never A.** MedSecure Health remains accountable for its regulatory obligations even when work is delegated — this is a core HIPAA principle (a covered entity can't outsource its liability) and a common gap in poorly-designed RACI matrices.
- **Workforce is mostly "I," with targeted "R" on data handling.** Most employees don't own GRC processes, but they are responsible for their own behavior (e.g., correctly classifying data they create, completing training).

---

## 4. Gaps This Surfaces (intentional — this is a real GRC skill)

Building this matrix should surface open questions a real GRC analyst would flag to leadership:

1. **Is there a dedicated Legal/Privacy Counsel role, or does this sit with outside counsel?** MedSecure Health's org chart hasn't specified this — worth deciding before this matrix is finalized.
2. **Does GRC report to the CISO or independently to the Board?** This matrix assumes GRC sits under/works closely with the CISO; some organizations separate these for independence. Worth a deliberate design decision, not a default.
3. **No dedicated Data Protection Officer (DPO) role exists.** Not required under HIPAA, but worth flagging as a watch-item if MedSecure ever expands into GDPR territory (per Deliverable 01's watch list).

---

## Next Step

Milestone 1 (Governance Charter) is now complete: Regulatory Landscape Map → Information Security Policy → RACI Matrix. Milestone 2 begins with the **ISO 27001 Scope Statement and Statement of Applicability (SoA)** — determining which Annex A controls apply to MedSecure Health and documenting the rationale for inclusion/exclusion of each.
