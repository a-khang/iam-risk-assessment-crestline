# New IAM processes for Crestline

## Process Scope
The proposed processes below reflect the scope of issues found in the CrestLine case.

### Joiners:
J1: **Role-based assignments for new employees**
 
<img width="1431" height="832" alt="image" src="https://github.com/user-attachments/assets/daff6435-c481-4c1f-8172-ad3ebd49f746" />

A major change proposed in this process is the inclusion of role-based profiles, which are predefined lists of resources that an employee must be able to access with respect to their role. It is the hiring manager's onus to determine a profile fits the new employee, or to initiate a consultation with Marcus who is more security-oriented. 
  
---

### Movers:
M1: **Responsive Role Transfers and Access Requests (IT must respond promptly to access requests)**

M2: **End-to-end Role Transfer validation** 
- (HR and IT changes must coincide before being written down officially into books - A ticketing system would help to track the status of role transfers for greater transparency)

---
### Leavers:
L1: **Project Site Closures in SharePoint**

L2: **Employee Departures**

L3: **Partner Departure**

--- 
* Identity Governance:
   * Temporary Access Management for Contractors, Temps, other external identities
   * Routine Access Reviews, not adhoc access reviews; Scope extends to departed identities to determine whether orphaned accounts exist
   * Access Revocation as a general curb against privilege creep and residual access; Proper, full closure of SharePoint sites will include revoking access to all project coordinators.

* Privileged Access Management
   * Unsure of what process needs to be captured here, but would definitely be written into a requirement for both IT staff, de facto or official system administrators, and Project Leads
 
## Considerations
* SSO integration across Crestline's SaaS via identity provider (ideally Microsoft Entra ID) would close gaps in revocation because accounts would be managed from a single platform. An account can be disabled which would suspend access across integrated systems immedietely. SSO support becomes a key requirement for IT solutions, whether they are built in-house or acquired off-shelf.
* A key issue highlighted in the case is remote access, which is very common among Crestline's consultants. While the scope of this project focused more on IAM process-related issues, remote access could be managed with ABAC (eg. time-based access) and detective controls.

## Questions
* Would user self-service for identities be feasible in an organization that moves fast and cannot easily afford more IT friction?
* Would stronger IT governance better orchestrate IT priorities in Crestline? Would the outcomes benefit IT operations, resources, business strategy alignment, or all?
