# Identity Security: A learning project
This project reflects my learnings of IAM and the role it plays in the cybersecurity strategy for organizations. I focus on the basic components of an Identity Security Program:
- **Identity Governance**
- **Authentication**
- **Authorization**
- **Accounting**

Goals:
- Define roles and an organization's need for IAM
- Develop a decision framework for defining base permissions, and cases for adjusting those 
- Document policies and procedures to define processes and rules (for joiner-mover-leaver, just-in-time access elevation, privileged access management, access reviews)
- Demo procedures and follow policies in Microsoft Entra ID (IAM active directory tool)

Under a simulated organizational scenario, I will:
- Define why the organization needs IAM, the risks that IAM will address, and who owns what (IT? HR? Managers? Security?)
- Establish the access control model, and the considerations for enforcement, exceptions, and change.
- Document policies, standards (JML, PAM, JIT) and procedures (Exception management, Access Review) to enforce in the IAM operating model.
- Configure Entra ID and demonstrate policy enforcement, control of privileged access, and procedures.

**Future Ideas**
- Tracking incidents involving privilege escalation
- Looking into non-human identities (and Agentic risks)
- CIEM

## Overview
This project documents the design and implementation of Identity Governance and Access Management for a small to mid-sized B2C SaaS organization providing personal analytics to end users. IAM needs to be grounded in facilitating the processes and people underlying the business, just as much as it needs to be grounded in risk. 

This project defines roles, identity populations, and governance rules before implementing IAM controls using Microsoft Entra. The focus is on establishing repeatable, mature identity processes such as joiner-mover-leaver lifecycle management, role-based access, privileged access governance, and access reviews. The outcome demonstrates how identity governance decisions are operationalized in Entra to support growth, protect user trust, and reduce identity-related risk.

Every deliverable is centred on a fictional business scenario that involves sensitive data and various roles.

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
