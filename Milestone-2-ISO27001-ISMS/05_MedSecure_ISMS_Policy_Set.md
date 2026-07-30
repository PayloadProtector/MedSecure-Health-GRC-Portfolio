# MedSecure Health — ISMS Policy Set

**Milestone 2, Deliverable 2** | GRC Portfolio Project
**Document Owner:** CISO / GRC Function
**Version:** 1.0
**Effective Date:** July 2026

---

## Overview

This document contains three sub-policies referenced in the Information Security Policy (Deliverable 02) — Access Control, Incident Response, and Acceptable Use — plus the ISMS Management Review Process. Each sub-policy maps back to specific Annex A controls from the Statement of Applicability (Deliverable 04) and, where relevant, to HIPAA requirements.

---

## 1. Access Control Policy

**Maps to:** ISO 27001 Annex A.5, A.8 | HIPAA Security Rule §164.312(a) (Access Control)

### 1.1 Purpose
Ensures that access to systems containing PHI or CHD is granted based on job necessity, reviewed regularly, and revoked promptly when no longer needed.

### 1.2 Policy Requirements

| Requirement | Detail |
|---|---|
| Least privilege | Users are granted the minimum access necessary to perform their job function |
| Role-based access | Access is assigned via defined roles (e.g., "Clinical Support," "Claims Processor"), not ad hoc per-user grants |
| Unique user IDs | Shared or generic accounts are prohibited for any system touching PHI |
| Multi-factor authentication (MFA) | Required for all remote access and all access to systems containing PHI or CHD |
| Access provisioning | New access requires manager approval and is logged |
| Access review | Quarterly review of all access to PHI-handling systems, performed by GRC with manager attestation |
| Deprovisioning | Access is revoked within 24 hours of termination or role change |
| Privileged access | Administrative accounts are separate from standard user accounts and subject to additional logging |

### 1.3 Rationale
HIPAA's Security Rule specifically requires access controls as a "required" implementation specification, not merely "addressable" — meaning MedSecure has no discretion on whether to implement this; only on the specific technical mechanism used.

---

## 2. Incident Response Policy

**Maps to:** ISO 27001 Annex A.5.24–28 | HIPAA Breach Notification Rule

### 2.1 Purpose
Defines how MedSecure Health detects, responds to, and reports security incidents, with particular attention to the legal timelines triggered by a PHI breach.

### 2.2 Incident Classification

| Severity | Definition | Example |
|---|---|---|
| Critical | Confirmed unauthorized access to PHI/CHD, or system-wide outage | Database breach exposing patient records |
| High | Suspected unauthorized access, significant service degradation | Suspicious login pattern on admin account |
| Medium | Policy violation without confirmed data exposure | Employee emails PHI to personal account |
| Low | Minor anomaly, no data or availability impact | Failed login attempts within normal thresholds |

### 2.3 Response Process

1. **Detection** — via monitoring tools, employee report, or third-party notification
2. **Triage** (target: within 4 hours of detection) — Security Ops assesses severity and scope
3. **Containment** — isolate affected systems/accounts
4. **Investigation** — determine root cause, scope of data involved, number of individuals affected
5. **Legal/Compliance determination** — Legal, in consultation with CISO, determines whether the incident meets the legal definition of a "breach" under HIPAA
6. **Notification** (if applicable):
   - Affected individuals: within 60 days of discovery
   - HHS: within 60 days (or annually if under 500 records)
   - Media: required if breach affects 500+ residents of a state/jurisdiction
7. **Post-incident review** — root cause documented, remediation tracked, lessons feed back into risk register

### 2.4 Rationale
The 60-day notification clock is a hard legal deadline under HIPAA — this policy is written to ensure triage happens fast enough that the organization doesn't lose track of that timeline during the chaos of an actual incident.

---

## 3. Acceptable Use Policy

**Maps to:** Internal governance | Supports FTC Act Section 5 obligations (accurate representations to consumers about data handling)

### 3.1 Purpose
Sets expectations for how workforce members use MedSecure Health systems, devices, and data.

### 3.2 Key Requirements

- Company systems are for business use; incidental personal use is permitted but must not create security risk
- PHI must never be transmitted via personal email, personal cloud storage, or unencrypted channels
- Removable media (USB drives, etc.) is prohibited for storing PHI, consistent with the A.7.10 exclusion in the SoA (MedSecure's environment is cloud-native by design)
- Workforce members must lock devices when unattended and report lost/stolen devices within 1 hour
- Use of unauthorized ("shadow IT") applications to process PHI is prohibited without GRC review and approval
- Social media and public communications about MedSecure Health's security posture require Legal/Communications approval

### 3.3 Rationale
Even well-designed technical controls fail if workforce behavior routes around them — this policy exists to close that human gap explicitly rather than assuming good judgment will suffice.

---

## 4. ISMS Management Review Process

**Maps to:** ISO 27001 Clause 9.3 (Management Review)

### 4.1 Purpose
Ensures leadership formally reviews the ISMS at planned intervals to confirm it remains suitable, adequate, and effective.

### 4.2 Frequency
Quarterly, with an annual comprehensive review.

### 4.3 Standing Agenda

1. Status of actions from previous management reviews
2. Changes in external/internal issues relevant to the ISMS (e.g., new regulations, business changes — cross-reference the Regulatory Landscape Map watch list)
3. Feedback on ISMS performance:
   - Nonconformities and corrective actions
   - Monitoring/measurement results (e.g., training completion rates, incident metrics)
   - Audit results (internal and external)
   - Achievement of security objectives (from Information Security Policy Section 5)
4. Feedback from interested parties (customers, regulators, partners)
5. Risk assessment results and status of risk treatment plan
6. Opportunities for continual improvement

### 4.4 Outputs
Management review must produce documented decisions on:
- Changes to the ISMS scope or SoA
- Resource needs
- Updates to security objectives
- Changes to risk appetite

### 4.5 Rationale
This is what keeps the ISMS a living system rather than a one-time compliance exercise — auditors specifically check that management review is happening on schedule with real decisions coming out of it, not just a meeting that occurred.

---

## Traceability Summary

| Sub-Policy | Primary Legal/Framework Driver |
|---|---|
| Access Control | HIPAA §164.312(a); ISO 27001 A.5, A.8 |
| Incident Response | HIPAA Breach Notification Rule; ISO 27001 A.5.24-28 |
| Acceptable Use | FTC Act Section 5; internal governance |
| Management Review | ISO 27001 Clause 9.3 |

---

## Next Step

With the ISMS policy set complete, Milestone 2 is now finished: Scope Statement & SoA → ISMS Policy Set. Milestone 3 begins with building the **Risk Register** — identifying, scoring, and documenting treatment decisions for MedSecure Health's top risks.
