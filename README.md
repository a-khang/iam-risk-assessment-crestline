# Identity Security: A learning project
This project reflects my learnings of IAM and the role it plays in the cybersecurity strategy for organizations. I focus on the basic components of an Identity Security Program:
- **Identity Governance**
- **Authentication**
- **Authorization**
- **Accounting**

I will:
- Define roles and an organization's need for IAM
- Develop a decision framework for defining base permissions and define business cases for adjusting role bases. This serves as an artifact which gets assessed in audits
- Document policies and procedures to define processes and rules (for joiner-mover-leaver, just-in-time access elevation, privileged access management, access reviews)
- Demo procedures and follow policies in Microsoft Entra ID (IAM active directory tool)

**Updates**
- Feb: These are the things that I wanted to specifically explore, especially from a business view of such a program. For the future, I may add additional demos and writeups exploring CIEM, potentially incident management. 

## Overview
This project documents the design and implementation of Identity Governance and Access Management for a small to mid-sized B2C SaaS organization providing personal analytics to end users. IAM needs to be grounded in facilitating the processes and people underlying the business, just as much as it needs to be grounded in risk. 

This project defines roles, identity populations, and governance rules before implementing IAM controls using Microsoft Entra. The focus is on establishing repeatable, mature identity processes such as joiner-mover-leaver lifecycle management, role-based access, privileged access governance, and access reviews. The outcome demonstrates how identity governance decisions are operationalized in Entra to support growth, protect user trust, and reduce identity-related risk.

Every deliverable is centred on a fictional business scenario that involves sensitive data and various roles.

## Scope
| In | Out |
| -- | -- |
|Organizational/governance artifacts; Documented processes; Entra implementation artifacts|Full Entra IaC; Complex multitenant or hybrid identity scenarios; Deep regulatory compliance mapping|

## Deliverables
### <a href="https://github.com/a-khang/identity_security/blob/main/part1.md/">1. Organizational and governance artifacts</a>
- Organizational context and business scenario description  
- Identity populations and role definitions  
- Risk-based access tier model  
- IAM and IGA policy document covering lifecycle, RBAC, access reviews, and privileged access  

### <a href="https://github.com/a-khang/identity_security/blob/main/part2.md/">2. Process documentation</a>
- Joiner, mover, leaver lifecycle flows  
- Access request and approval logic  
- Privileged access request and activation flow  
- Exception handling and temporary access process  
- Access review cadence and remediation steps  

### <a href="https://github.com/a-khang/identity_security/blob/main/part3.md/">3. Entra implementation artifacts</a>
- Entra tenant structure overview  
- Group-based RBAC model aligned to risk tiers  
- Application access assignments using groups  
- Privileged Identity Management configuration  
- Access Review configuration by role and risk level  
- Non-human identity governance approach.

### <a href="https://github.com/a-khang/identity_security/blob/main/part4.md/">4. Evidence of repeatability</a> 
- Examples of group-based access enforcement  
- Sample access review outputs and decisions  
- Before and after access states for lifecycle events  
- Clear mapping from governance rule to Entra control 
