# IAM Case Study: Crestline Advisory Group
**A Fictional Organization | For Portfolio & Analysis Use**

---

## Organization Overview

Crestline Advisory Group is a 90-person management consulting firm headquartered in Vancouver, BC. The firm advises mid-market clients in the financial services and real estate sectors on operational strategy, regulatory compliance, and process improvement. Approximately 60% of staff are client-facing consultants; the remainder work in operations, finance, HR, and IT.

Crestline operates under moderate regulatory pressure. As a holder of client financial data and confidential business strategy documents, the firm is contractually obligated under several client NDAs to maintain reasonable information security controls. Two of its largest clients are federally regulated financial institutions that conduct annual vendor assessments, which Crestline must respond to.

The firm has grown from 40 to 90 employees over the past three years, primarily through lateral hires from larger consulting firms and two small acquisitions.

---

## Organizational Structure

| Group | Size | Key Responsibilities |
|---|---|---|
| Consulting (Senior & Junior) | 54 | Client delivery, travel, remote work common |
| Operations & Finance | 14 | Internal reporting, procurement, billing |
| Human Resources | 6 | Hiring, onboarding, offboarding, performance |
| Information Technology | 5 | Infrastructure, helpdesk, SaaS administration |
| Leadership (Partners) | 7 | Business development, client relationships, firm strategy |

The IT team is led by a single IT Manager, Marcus, who reports to the COO. There is no dedicated security function. Compliance and security inquiries from clients are handled by Marcus in coordination with the COO.

---

## Technology Environment

Crestline operates primarily in the Microsoft 365 ecosystem. Core platforms and their purposes are as follows:

- **Microsoft 365 (Exchange, Teams, SharePoint, OneDrive)** — Communication and document collaboration. Client deliverables and working files are stored in SharePoint project sites.
- **BambooHR** — HR system of record. Used for employee lifecycle tracking, org chart, and leave management.
- **Salesforce** — CRM. Used by Partners and senior consultants to manage client relationships, pipeline, and engagement records. Contains client contact information and revenue data.
- **Mavenlink (now Kantata)** — Project management and resource allocation. Tracks billable hours, project staffing, and engagement timelines.
- **QuickBooks Online** — Finance and accounting. Accessed by the Finance team and the COO.
- **Zoom** — External client calls. Separate from Teams, maintained for client preference reasons.

Most SaaS platforms are administered directly by Marcus or, in some cases, by the application's primary business owner (e.g., the HR Director manages BambooHR; the Sales Operations lead manages Salesforce).

---

## Normal Course of Business: Key Workflows

### Hiring & Onboarding
When Crestline hires a new employee, HR initiates the process by sending a welcome email to IT with the new hire's name, start date, job title, and department. IT creates their Microsoft 365 account and grants access based on what the hiring manager verbally requests, typically over Teams chat or a quick call. The new hire's first day usually includes a laptop setup session with IT and an HR orientation covering policies and benefits.

Consultants are frequently onboarded directly into active client engagements and are granted SharePoint access to relevant project sites by their project lead, who has owner-level permissions on those sites.

Senior hires and lateral transfers from other firms sometimes arrive with their own working files or templates, which they upload to SharePoint or OneDrive for use on new engagements.

### Employee Transfers & Role Changes
Crestline promotes internally and periodically restructures project teams. When a consultant moves from a junior to a senior role, or shifts from one practice area to another, the change is recorded in BambooHR by HR. The hiring manager notifies IT informally if additional system access is needed for the new role, though this does not always happen promptly.

Consultants routinely collaborate across practice areas and are often added to SharePoint project sites for engagements outside their primary team for the duration of a project.

### Client Engagement Lifecycle
Each client engagement is supported by a dedicated SharePoint site containing working documents, client data extracts, and draft deliverables. Project leads are responsible for managing site membership. When an engagement concludes, the project lead archives the deliverable and notifies the Operations team for billing closure. SharePoint site access is not formally reviewed or revoked as part of engagement closeout.

### Offboarding
When an employee resigns or is terminated, HR notifies IT by email, typically on or shortly before the employee's last day. IT disables the Microsoft 365 account and retrieves the employee's laptop. BambooHR is updated to reflect the departure.

The offboarding process is largely handled between HR and IT on an ad hoc basis. There is no formal checklist. IT focuses primarily on the Microsoft 365 account and device; downstream SaaS platforms are addressed if someone thinks to mention them.

Partners are rarely subject to formal offboarding processes, as their departures are negotiated confidentially and handled by the COO directly.

---

## Staffing Patterns & Operational Notes

- Consultants frequently work remotely and from client sites. It is common for a consultant to work on two to three concurrent client engagements.
- The firm experiences meaningful turnover at the junior consultant level, with average tenure of approximately 18–24 months.
- Contract and temporary staff are occasionally brought in during high-demand periods to support specific engagements. These individuals are set up with Microsoft 365 accounts and granted project-specific access by IT upon request from the engagement lead.
- Two employees acquired through a 2022 acquisition — one now in Operations, one who departed eight months ago — were originally provisioned under the acquired firm's naming conventions before being migrated to Crestline's systems.
- Marcus, the IT Manager, is the sole administrator for most SaaS platforms. During a period of extended leave last year, administrative access to several platforms was temporarily shared with a senior consultant to ensure continuity.
- Crestline does not currently conduct periodic access reviews. The last comprehensive review of user accounts across platforms was performed during a client vendor assessment response approximately 14 months ago.

---

*This case is fictional. All names, figures, and organizational details are invented for analytical and portfolio purposes.*
