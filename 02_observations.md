# Observations & Inferences: Crestline Advisory Group
**IAM Case Analysis | Stage 1 of 4**

---

## Overview

The following observations are drawn from a close reading of Crestline Advisory Group's organizational structure, technology environment, and operational workflows. Where the case describes process, this analysis identifies what those descriptions assume, omit, or contradict. Findings are organized thematically rather than by workflow to surface the underlying causes of access management risk at Crestline.

---

## 1. Fragmented Access Governance

Access decision-making at Crestline is distributed across multiple groups without clear ownership, consistent criteria, or a security function to provide oversight.

For standard onboarding, access is determined by the hiring manager, who communicates requirements to IT verbally or via Teams chat. No role-based access model is described, which means there is no defined baseline of what access a given role should carry. Whether a hiring manager has the awareness to request only what is necessary — and nothing more — is an assumption the process makes without validating. IT implements what it is told; there is no evidence that Marcus reviews or challenges access requests on security grounds.

Within Microsoft 365, SharePoint project site membership is managed by project leads rather than IT. This represents a delegation of access control to individuals who are not accountable for security outcomes and are unlikely to apply consistent standards. The case does not suggest that project leads receive guidance on access management principles or that their decisions are reviewed.

For several SaaS platforms, administrative access is held by the application's primary business owner rather than IT. This means access control within those systems — including who can grant, modify, or revoke access — sits with individuals whose primary accountability is operational, not security-oriented.

The IT Manager, Marcus, is the de facto security function at Crestline. He is the primary SaaS administrator and the person to whom security-related client inquiries are escalated. However, the case does not establish that Marcus is consistently consulted in provisioning decisions, nor that he has the capacity or authority to enforce access standards across a decentralized environment. When access-related failures occur, accountability will likely fall on Marcus regardless of whether the decisions that caused them were his to make.

---

## 2. Lifecycle Process Gaps

The joiner, mover, and leaver processes at Crestline share a common weakness: they are narrowly scoped, informally triggered, and not consistently executed across the full range of systems and user populations.

**Joiner**
Onboarding is initiated when HR emails IT with basic employee information. A second trigger — the hiring manager's verbal access request — is required before IT can complete provisioning. The case does not describe what prompts the hiring manager to make this request, or how quickly it occurs relative to the employee's start date. This introduces latency risk and creates a dependency on informal coordination. Consultants onboarded directly into active engagements receive SharePoint project site access granted by their project lead, outside of any IT-managed process.

**Mover**
Role changes and internal transfers are recorded in BambooHR, but IT is only notified if the hiring manager proactively reaches out. The case acknowledges this does not always happen promptly. Two consequences follow: access appropriate to the new role may be delayed, and access tied to the previous role may never be removed. The case does not describe any mechanism for reviewing or revoking prior access when a consultant's responsibilities change. Over time, and given Crestline's pattern of cross-practice collaboration, individual consultants are likely to accumulate access well beyond what their current role requires.

**Leaver**
Offboarding is triggered by HR notifying IT on or shortly before an employee's last day. The process has no formal checklist and is handled ad hoc. IT's focus is on Microsoft 365 account disablement and device retrieval. Downstream SaaS platforms — Salesforce, BambooHR, Mavenlink, QuickBooks, Zoom — are addressed only if someone thinks to raise them. There is no evidence that SharePoint project site membership is reviewed or revoked as part of offboarding.

Partner departures represent a distinct gap. These are handled confidentially by the COO and do not follow any described IT process. It is not established that IT is notified, or that access across any system is formally revoked upon a partner's departure.

A further gap exists for contractors and temporary staff, who are provisioned with Microsoft 365 accounts and project-specific access on request, but for whom no distinct offboarding process is described.

---

## 3. Accumulated & Unreviewed Access

The cumulative effect of the governance and lifecycle gaps above is a user access landscape that has grown without systematic review or remediation.

Consultants routinely work across multiple concurrent engagements and are added to SharePoint project sites for the duration of each. The case does not describe any process for removing this access when an engagement concludes. Engagement closeout procedures are limited to billing closure; SharePoint site access is not formally reviewed or revoked. A consultant with two or three years of tenure at Crestline may retain access to dozens of project sites containing client intellectual property, financial data, and confidential strategy documents — access that was appropriate at the time of granting but has not been revisited since.

The case notes that during Marcus's extended leave, administrative access to several SaaS platforms was temporarily shared with a senior consultant. Whether this access was revoked upon Marcus's return is not stated. Given the pattern of informal access management at Crestline, and the absence of any described access review process, it is reasonable to infer that this elevated access may still be active. The identity and current employment status of the senior consultant involved is not confirmed.

Two employees from a 2022 acquisition were provisioned under legacy naming conventions before migration. One of these individuals departed eight months ago. Given the informality of Crestline's offboarding process and the non-standard account structure, it is not clear that this individual's access was comprehensively revoked across all platforms.

Crestline's last comprehensive access review was conducted approximately 14 months ago, in response to a client vendor assessment. No periodic review cadence is described, meaning the current access state has accumulated for over a year without a structured reconciliation against current roles and employment status.

---

## 4. Visibility & Accountability Gaps

Underlying all of the above is a systemic absence of visibility into who has access to what, and a diffusion of accountability that makes it difficult to detect or respond to access-related failures.

No described mechanism exists for producing a current, consolidated view of user access across Crestline's systems. SaaS administration is split between IT and business owners; SharePoint membership is managed by project leads; access decisions are made verbally and without documentation. In the event of a security incident or client vendor assessment, reconstructing the access history for a given user or system would require manual coordination across multiple teams.

The populations most likely to generate orphaned or excessive access — junior consultants with high turnover, contractors on short engagements, employees whose roles have shifted, and departing partners — are also the populations least well-served by Crestline's current processes. High turnover at the junior level in particular means that the volume of offboarding events is significant, and each one is an opportunity for access to persist beyond employment.

Project leads who manage SharePoint membership are not described as having any security awareness, training, or accountability for their access decisions. Their primary frame of reference is project delivery, not information security. The assumption that they will apply least-privilege principles or conduct access reviews at engagement closeout is not supported by anything in the case.

The practical consequence is that Marcus absorbs security accountability for outcomes that result from decisions made entirely outside his involvement. This is not sustainable, and it means that when a control fails — a terminated employee accessing a project site, a compromised shared admin credential, a client data exposure — the root cause will be structural rather than individual, but the visibility to identify that in advance does not currently exist.

---

*This writeup informs the risk register developed in Stage 2. Each theme above maps to one or more IAM risk categories: orphaned accounts, excessive privilege, shared credentials, inadequate offboarding, absence of access reviews, and informal provisioning.*
