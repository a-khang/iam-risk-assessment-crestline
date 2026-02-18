# Entering the Scenario & the Strategic Needs for IAM

## Background
Insightra is an 80-person company that develops software products specialized in personal analytics. The platform aggregates user-provided data and behavioral signals to generate individualized insights and recommendations. Originally a team of fewer than 20 employees, Insightra found product-market fit and is now scaling rapidly in response to growing demand. The company raised a $4-8M Seed round to validate its product, followed by a $15-25M Series A to expand engineering, data infrastructure, and go-to-market operations.
### Team Growth:
- To expand service capacity and innovation, they have scaled their teams across software engineering, IT, and R&D.
- The operations side has also grown their teams across, finance, marketing, sales, and customer service.
- HR, a function responsible for handling payroll, managing the employee lifecycle, and fostering a positive work environment, has also scaled to operate for a larger company.
### Insightra’s Strategic Needs:
- It is likely that Insightra had very informal or ad-hoc access management to foster the high degree of collaboration and cross-functionality needed to bring the company its successes. This would be harder to maintain now for a larger, 80-person company. The need for formal IAM comes down to governance expectations from investors, mitigating invisible risk from informal access, and facilitating auditability. At this stage, Insightra cares about stakeholder confidence.
- As Insightra grows, productivity should be maintained and supported (not constrained) in a system that increases controls around identity and access. This is important as Insightra seeks to balance cross-functionality and the separation of duties.
- Although Insightra is outgrowing informal processes, cross-functionality is still needed to facilitate high collaboration. Users across multiple groups may be assigned across various projects, and resources normally assigned to certain roles may require exposure by someone not normally in that role. This could be someone internally from another department; someone externally such as a partner or contractor.
- People may join, transition into, and leave roles, projects, or the organization entirely. Accounts with access will need to be provisioned, adjusted, and decommissioned over time. Insightra wants to ensure that nobody has excessive access, and there are no decommissioned accounts with "shadow" access.
- Because Insightra handles personal/sensitive data (both internally and as a part of its product), having an enforced system of identity and access processes ensures that the exposure of data (and other resources) are controlled in a secure manner.
- Secure access should be seamless for internal users. Complexity incentivizes workarounds, which will undermine any IAM strategy that Insightra implements.

## Identity Governance & Developing Access Policy / Procedures

### Identity Lifecycle
#### Joiner
_Automate the creation of new accounts_
#### Mover
_Provide only the access necessary for transitioning between roles_
#### Leaver
_Remove access for accounts that no longer need it_

### User Access Reviews
_curbing the risk of privilege creep_
### Access Requests
_A system to manage access requests would provide Insightra with a record of who requested and who approved access, and when it took place_
1. Access Request
2. Manager Approval
3. Access Granted

### Role Management

### Segregation of Duties (P)
_Ensures that no single role will have complete control over a system or process_
