# MedSecure Health — Regulatory Landscape Map

**Milestone 1, Deliverable 1** | GRC Portfolio Project
**Prepared for:** MedSecure Health (fictional entity)
**Date:** July 2026

---

## 1. Company Profile & Scope Assumptions

MedSecure Health is a fictional healthcare technology company used as the basis for this GRC portfolio. Assumptions below define regulatory scope — in a real engagement, these would come from a scoping interview with the business.

| Attribute | Detail |
|---|---|
| Industry | Healthcare SaaS — patient portal, telehealth, insurance claims processing |
| Size | ~200 employees |
| Data handled | Protected Health Information (PHI) for ~50,000 patients; payment card data for premium subscriptions |
| Geographic footprint | Operating across multiple US states; no current EU patient base |
| Business model | B2C patient platform + B2B contracts with regional hospital networks |
| Cloud posture | AWS-hosted, multi-tenant SaaS architecture |

**Why this matters for the exercise:** a regulatory landscape map is only useful if it's scoped to what actually applies. A common mistake in GRC work (and in portfolio pieces) is listing every regulation that could theoretically apply. The value is in the *applicability reasoning* — showing you can justify why something is in scope, watch-list, or out of scope.

---

## 2. Regulatory Landscape — In Scope

| Law / Regulation | Type | Why It Applies to MedSecure | Key Obligations |
|---|---|---|---|
| **HIPAA Privacy Rule** | Federal law | MedSecure creates, stores, and transmits PHI as a covered entity/business associate | Minimum necessary use, patient access rights, authorization for disclosures |
| **HIPAA Security Rule** | Federal law | Same PHI handling as above, specifically addressing electronic PHI (ePHI) | Administrative, physical, and technical safeguards; risk analysis requirement (45 CFR §164.308(a)(1)) |
| **HIPAA Breach Notification Rule** | Federal law | Any unauthorized PHI disclosure triggers this | Notify affected individuals, HHS, and (if >500 records) media, within 60 days |
| **HITECH Act** | Federal law | Amends/strengthens HIPAA; applies directly given ePHI use | Increases breach penalties, extends liability to business associates, incentivizes audit trails |
| **FTC Act, Section 5 (unfair/deceptive practices)** | Federal law | Applies to any US company; FTC has pursued health data cases (esp. for data outside strict HIPAA coverage, e.g. wellness app data) | Requires that privacy/security claims made to consumers are accurate and substantiated |
| **State breach notification laws** | State law (all 50 states have one) | MedSecure operates multi-state, so the strictest applicable state law governs each affected resident | Notification timelines vary (some as short as 30 days); may require state AG notification |
| **State health data privacy laws** (e.g., California CMIA, Washington My Health My Data Act) | State law | Several operating states have health-data-specific laws that layer on top of HIPAA | Broader definition of "health data" than HIPAA in some states; private right of action in some cases |
| **PCI-DSS** | Industry standard (contractual, not law) | MedSecure processes payment card data for subscriptions | Network segmentation, cardholder data protection, quarterly scans, annual assessment |

---

## 3. Regulatory Landscape — Watch List (Not Currently In Scope)

| Law / Regulation | Why It's Not In Scope Today | Trigger That Would Bring It In Scope |
|---|---|---|
| **GDPR** | No EU patients or EU data processing currently | Expansion to EU market, or processing data of any EU resident |
| **42 CFR Part 2** (substance use disorder records) | MedSecure's platform doesn't currently handle SUD treatment records | Adding a behavioral health / addiction treatment service line |
| **FDA Software as a Medical Device (SaMD) regulations** | Platform is currently informational/administrative, not diagnostic | If any feature crosses into clinical decision support or diagnosis |
| **SOX (Sarbanes-Oxley)** | MedSecure is assumed privately held | If MedSecure goes public, financial reporting controls become mandatory |
| **CCPA/CPRA** | Most health data is already carved out under HIPAA overlap, but this should be re-checked as CA-specific exposure grows | Significant scale-up of CA consumer base or non-HIPAA-covered data collection |

*(This "watch list" section is intentionally included — it's a strong interview signal that you understand regulatory scope isn't static, and it's a place where a real GRC analyst adds ongoing value.)*

---

## 4. Voluntary Frameworks & Standards Layered On Top

These aren't legally mandated but are strongly expected in healthcare tech and will anchor the rest of this project:

| Framework | Role in MedSecure's Program |
|---|---|
| **ISO 27001** | Provides the overarching ISMS structure — governance, risk treatment, Statement of Applicability. Chosen as the primary framework for Milestone 2. |
| **NIST 800-53** | Provides granular technical/operational control depth, especially useful for mapping to a Moderate baseline given ePHI sensitivity. Used in Milestone 4. |
| **HITRUST CSF** | Industry-specific meta-framework that harmonizes HIPAA, NIST, and ISO for healthcare — worth knowing exists, referenced but not built out in this project to keep scope focused. |
| **SOC 2 (Type II)** | Common client/partner requirement for healthcare SaaS vendors; informs the Capstone audit report in Milestone 5. |

---

## 5. Summary Table — Applicability at a Glance

| Category | Count | Examples |
|---|---|---|
| Federal law (mandatory) | 4 | HIPAA Privacy/Security/Breach, HITECH |
| State law (mandatory, varies by state) | 2 categories | Breach notification, health data privacy |
| Contractual/industry standard (mandatory) | 1 | PCI-DSS |
| Voluntary framework (strategic choice) | 3 | ISO 27001, NIST 800-53, SOC 2 |
| Watch list (not yet triggered) | 5 | GDPR, 42 CFR Part 2, FDA SaMD, SOX, CCPA/CPRA |

---

## Next Step

This map feeds directly into **Milestone 1, Deliverable 2: Information Security Policy**, which will need to explicitly reference HIPAA Security Rule safeguards and set the foundation for the ISO 27001 ISMS scope in Milestone 2.
