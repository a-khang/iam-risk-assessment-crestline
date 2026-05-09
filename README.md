# IAM Risk Assessment & Process Design
**Crestline Advisory Group | Independent Portfolio Project**

---

## Overview

This project simulates an end-to-end identity and access management (IAM) risk assessment for a fictional 90-person management consulting firm operating in the Microsoft 365 ecosystem. It was designed to practice GRC methodology — moving from organizational observation through risk identification, control gap analysis, and future-state process design.

The assessment follows a four-stage analytical workflow, each stage building directly on the last. All findings, risk entries, and control mappings are grounded in a fictional case study developed for this purpose.

---

## Objectives

- Apply structured analytical thinking to surface implied IAM risks from an organizational context
- Build a scored risk register scoped to identity and access management, tied to real assets and threat scenarios
- Benchmark current-state practices against NIST CSF 2.0 and NIST SP 800-53 control families
- Design a future-state JML (Joiner/Mover/Leaver) workflow that resolves identified control gaps

---

## Scope

**Organization:** Crestline Advisory Group — a fictional management consulting firm  
**Environment:** Microsoft 365 (SharePoint, Exchange, Teams, OneDrive), Salesforce, BambooHR, Mavenlink, QuickBooks Online, Zoom  
**User populations in scope:** Full-time employees, contractors and temporary staff, acquired employees, departing partners  
**IAM lifecycle coverage:** Joiner, Mover, Leaver  
**Control frameworks:** NIST Cybersecurity Framework (CSF) 2.0 — GV and PR outcome categories; NIST SP 800-53 Rev. 5 — AC and PM control families  

---

## Project Structure

```
iam-risk-assessment-crestline/
│
├── 01_case-study/
│   └── crestline-case-study.md          # Fictional organization context, workflows, and operational notes
│
├── 02_observations/
│   └── observations-and-inferences.md   # Stage 1 — Structured analysis of implied process gaps and governance failures
│
├── 03_risk-register/
│   └── 03_risk-register.xlsx               # Stage 2 — Scored risk register with asset, risk, likelihood, impact, owner, status, and control references, with Control gap analysis mapped to NIST CSF outcomes and SP 800-53 controls
│
├── 04_process-map/ (IN PROGRESS)
│   └── jml-future-state.drawio          # Stage 4 — Future-state JML workflow in draw.io with swimlane structure
│   └── jml-future-state.png             # Exported diagram for viewing without draw.io
│
└── README.md
```

---

## Methodology

### Stage 1 — Observations & Inferences
The case study was read as an analyst rather than a student — identifying where process descriptions end and assumptions begin, where accountability transfers between groups without clear ownership, and which user populations fall outside standard workflows. Findings were organized into four themes: fragmented access governance, lifecycle process gaps, accumulated and unreviewed access, and visibility and accountability gaps.

### Stage 2 — Risk Register
Observations were formalized into nine risk entries across six asset categories: client intellectual property, financial records, systems, reputational trust, contractual standing, and operational integrity. Each entry includes a threat scenario grounded in the case, a likelihood and impact score on a 3x3 matrix with written rationale, an IAM risk category, an assigned owner by role, a remediation status, and mapped CSF outcomes and 800-53 controls.

### Stage 3 — Gap Analysis
Each risk register entry was mapped to one or more NIST CSF 2.0 outcome subcategories (primarily GV.RR, GV.PO, GV.OC, and PR.AA) and corresponding SP 800-53 Rev. 5 controls across the AC and PM families. Control citations were scoped to entries where the case provides sufficient evidentiary basis — overcitation was treated as a credibility problem, not a thoroughness signal.

### Stage 4 — Process Design
A future-state JML workflow was designed in draw.io using swimlanes organized by organizational group (HR, IT/Security, Hiring Manager). Every process step is traceable to a specific gap identified in Stage 3. Trigger events, approval gates, and verification steps are explicitly represented. Non-standard populations — contractors, acquired employees, and departing partners — are handled as named branches rather than footnotes.

---

## Key Findings

- Access decision-making is distributed across HR, IT, project leads, and SaaS business owners without defined ownership criteria or security oversight, creating systemic accountability gaps
- The joiner, mover, and leaver lifecycle is scoped narrowly to Microsoft 800-53 account management and device retrieval; downstream SaaS platforms are addressed inconsistently or not at all
- Consultants accumulate SharePoint project site access across engagements with no revocation trigger at engagement closeout; archiving a site does not revoke membership
- An administrative credential of unknown revocation status was granted to a senior consultant during the IT Manager's extended leave, representing unmanaged privileged access outside IT's visibility
- Partner departures bypass IT entirely, leaving high-privilege accounts potentially active across Salesforce and Microsoft 365 with no described revocation process
- The last comprehensive access review was conducted 14 months prior to assessment, in response to a client vendor assessment rather than as a scheduled control

---

## Controls Referenced

| Family | Controls |
|---|---|
| NIST SP 800-53 — Access Control (AC) | AC-1, AC-2, AC-2(7), AC-3, AC-5, AC-6, AC-13, AC-21, AC-24 |
| NIST SP 800-53 — Audit & Accountability (AU) | AU-9, AU-12 |
| NIST SP 800-53 — Program Management (PM) | PM-1, PM-2, PM-9, PM-13, PM-23 |
| NIST CSF 2.0 — Govern | GV.PO-01, GV.PO-02, GV.RR-01, GV.RR-02, GV.RR-04, GV.OC-03, GV.RM-06 |
| NIST CSF 2.0 — Protect | PR.AA-01, PR.AA-05, PR.AT-02 |
| NIST CSF 2.0 — Identify | ID.AM-08, ID.RA-04, ID.RA-06 |

---

## Tools Used

- **Microsoft Excel** — Risk register construction and scoring
- **draw.io** — Future-state JML process mapping
- **Markdown** — Case study, observations, gap analysis memo, and documentation
- **NIST CSF 2.0 Reference Tool** — CSF outcome mapping
- **NIST SP 800-53 Rev. 5** — Control family reference

---

## Limitations

This project is based on a fictional case study designed to surface realistic IAM risks in a mid-size professional services context. Findings and control mappings reflect the information available in the case — no primary research, interviews, or system access were conducted. Control citations are scoped to gaps with sufficient evidentiary basis in the case material; gaps that could not be supported by specific case evidence were excluded.

---

## About

Developed independently as a portfolio project during a career transition toward cybersecurity GRC and consulting. The author is a Business Technology Management student at the UBC Sauder School of Business holding a CompTIA Security+ certification.
