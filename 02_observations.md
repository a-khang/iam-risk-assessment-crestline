# Observations & Inferences: Crestline Advisory Group
**IAM Case Analysis | Stage 1 of 4**

---

## Overview

The following observations are drawn from a close reading of Crestline Advisory Group's organizational structure, technology environment, and operational workflows. Where the case describes process, this analysis identifies what those descriptions assume, omit, or contradict. Findings are organized thematically rather than by workflow to surface the underlying causes of access management risk at Crestline.

---

## 1. Fragmented Access Governance

No policy governs how access is requested, approved, or revoked. Security accountability is informally concentrated in Marcus without the authority, mandate, or visibility to enforce standards across a decentralized environment. Since Marcus does not directly interface with leadership, IT issues like security are only viewed from an operational lens, which leaves a major blind spot for access risks culminating into contractual/legal issues (among other security problems).

Marcus might not have the power or trust to enforce security policies consistently, and it can be well assumed that there isn't a standard method for access decisions across HR, IT, project leads, and SaaS owners.

---

## 2. Lifecycle Process Gaps

The joiner, mover, and leaver processes at Crestline exhibit several weaknesses: 
- Verbal provisioning requests lack standardization and auditability
- Role-based access baselines undefined at onboarding
- Mover process recorded in HR but not operationalized in IT
- Residual access from prior roles never formally revoked
- Leaver process scoped to M365 only — downstream SaaS platforms unaddressed
- Partner departures bypass IT entirely
- Contractor and temporary staff have no defined offboarding trigger

**Joiner**
Onboarding is initiated when HR emails IT with basic employee information. A second trigger (the hiring manager's verbal access request) is required before IT can complete provisioning. The case does not describe what prompts the hiring manager to make this request, or how quickly it occurs relative to the employee's start date. This introduces latency risk and creates a dependency on informal coordination. 

Consultants onboarded directly into active engagements receive SharePoint project site access granted by their project lead, outside of any IT-managed process.

**Mover**
Role changes and internal transfers are recorded in BambooHR, but IT is only notified if the hiring manager proactively reaches out. The case acknowledges this does not always happen promptly. Two consequences follow: access appropriate to the new role may be delayed, and access tied to the previous role may never be removed. The case does not describe any mechanism for reviewing or revoking prior access when a consultant's responsibilities change. 

Over time, and given Crestline's pattern of cross-practice collaboration, individual consultants are likely to accumulate access well beyond what their current role requires.

**Leaver**
Offboarding is triggered by HR notifying IT on or shortly before an employee's last day. The process has no formal checklist and is handled ad hoc. IT's focus is on Microsoft 365 account disablement and device retrieval. Downstream SaaS platforms (Salesforce, BambooHR, Mavenlink, QuickBooks, Zoom) are addressed only if someone thinks to raise them. There is no evidence that SharePoint project site membership is reviewed or revoked as part of offboarding.

Partner departures represent a distinct gap. These are handled confidentially by the COO and do not follow any described IT process. It is not established that IT is notified, or that access across any system is formally revoked upon a partner's departure.

A further gap exists for contractors and temporary staff, who are provisioned with Microsoft 365 accounts and project-specific access on request, but for whom no distinct offboarding process is described.

---

## 3. Accumulated & Unreviewed Access

The cumulative effect of the governance and lifecycle gaps above is a user access landscape that has grown without systematic review or remediation.

### SharePoint Access: Consultants
Consultants routinely work across multiple concurrent engagements and are added to SharePoint project sites for the duration of each. The case does not describe any process for removing this access when an engagement concludes. Engagement closeout procedures are limited to billing closure; SharePoint site access is not formally reviewed or revoked. 

- A consultant with two or three years of tenure at Crestline may retain access to dozens of project sites containing client intellectual property, financial data, and confidential strategy documents. That access that was appropriate at the time of granting but has not been revisited since.

### SharePoint Access: Project Leads
This issue also touches on project lifecycles, which is governed by project leads and entirely outside the scope of IT governance. The issue isn't decentralization per se, as the firm requires a lot of operational flexibility to deliver services to clients without burdening IT. Instead, the issue is a lack of governance that makes this strategy secure.
- Individual-level site permissions unmanageable at scale: Leads to inconsistencies in provisioning individual access to consultants, instead of using group-based access model.
- Project leads hold owner-level access without defined responsibilities or best practice guidance
- Site membership not revoked at engagement closeout: Archiving does affect read- and write-level access, but does address owner access. Archived sites retain confidential client data indefinitely with no retention policy, and if an owner can freely access project resources after the end of an engagement, that's considered orphaned access.

### Residual Privileged Access from Temporary Leave

The case notes that during Marcus's extended leave, administrative access to several SaaS platforms was temporarily shared with a senior consultant. Whether this access was revoked upon Marcus's return is not stated. Given the pattern of informal access management at Crestline, and the absence of any described access review process, it is reasonable to infer that this elevated access may still be active. The identity and current employment status of the senior consultant involved is not confirmed.

### Acquired Employees

Two employees from a 2022 acquisition were provisioned under legacy naming conventions before migration. One of these individuals departed eight months ago. Given the informality of Crestline's offboarding process and the non-standard account structure, it is not clear that this individual's access was comprehensively revoked across all platforms.

Crestline's last comprehensive access review was conducted approximately 14 months ago, in response to a client vendor assessment. No periodic review cadence is described, meaning the current access state has accumulated for over a year without a structured reconciliation against current roles and employment status.

---

## 4. Visibility & Accountability Gaps

Underlying all of the above is a systemic absence of visibility into who has access to what, and a diffusion of accountability that makes it difficult to detect or respond to access-related failures.

No described mechanism exists for producing a current, consolidated view of user access across Crestline's systems.
- SaaS administration is split between IT and business owners; SharePoint membership is managed by project leads
- Access decisions are made verbally and without documentation
- In the event of a security incident or client vendor assessment, reconstructing the access history for a given user or system would require manual coordination across multiple teams.

The populations most likely to generate orphaned or excessive access (i.e. junior consultants with high turnover, contractors on short engagements, employees whose roles have shifted, and departing partners) are also the populations least well-served by Crestline's current processes. High turnover at the junior level in particular means that the volume of offboarding events is significant, and each one is an opportunity for access to persist beyond employment.

Project leads who manage SharePoint membership are not described as having any security awareness, training, or accountability for their access decisions. Their primary frame of reference is project delivery, not information security. The assumption that they will apply least-privilege principles or conduct access reviews at engagement closeout is not supported by anything in the case.

### Potential Consequences

Access continues to accumulate without systemic reconciliation against current roles and employment status, leading to more excessive, dormant, and orphaned access. Departed employees, acquired firm staff, and contractors not consistently captured in review scope. Worse yet, there is no preiodic review cadence, and as a reactive measure triggered by client assessments rather than proactive internal governance.

Visibility and assurance to carry out security must hold leadership accountable, IT managers and resource owners responsible, and all levels employees involved. But these sort of scenarios unfortunately pin Marcus for sole liability given the nature of IT governance within Crestline, even if he is not empowered to lead security and compliance in he firm (sometimes you'd attribute this to constant IT firefighting which prevents coordination and collaboration).

IAM risks are detailed in Part 3, but they include:
- Non-compliance to information security requirements outlined in contracts/regulations -> Penalties
- Excessive privileges -> Increased exposure to threats of unauthorized access / data breach
