# Identity Security: A learning project
This project reflects my learnings of IAM and the role it plays in the cybersecurity strategy for organizations. I focus on the basic components of an Identity Security Program:
- **Identity Governance**
- **Authentication**
- **Authorization**
- **Accounting**

Under a simulated organizational scenario, I will:
- Define why the organization needs IAM, the risks that IAM will address, and who owns what (IT? HR? Managers? Security?)
- Establish the access control model, and the considerations for enforcement, exceptions, and change.
- Document policies, standards (JML, PAM, JIT) and procedures (Exception management, Access Review) to enforce in the IAM operating model.
- Configure Entra ID and demonstrate policy enforcement, control of privileged access, and procedures.

Goals for learning and growth:
- Explaining concepts clearly
- Demonstrate high-level and low-level thinking
- Be able to "solution" (recommend and justify) and how to design a cybersecurity solution in an organizational context

**Future Ideas**
- Tracking incidents involving privilege escalation
- Looking into non-human identities (and Agentic risks)
- CIEM

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
