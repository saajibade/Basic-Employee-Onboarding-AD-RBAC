# Basic Employee Onboarding (AD)(RBAC)

## Problem Statement
Northstar Medical Group's infrastructure was left severely compromised due to years of mismanagement by a third-party Managed Service Provider (MSP). The environment completely lacked structure, operating on a flat directory with manual, ad-hoc user provisioning that lacked standardized naming conventions or attribute consistency. Because there were no established security boundaries or role-based access controls, administrative access was unmonitored and file permissions were completely unmanaged. This severe technical deficit introduced massive operational inefficiencies and created critical security vulnerabilities, placing the organization at high risk for catastrophic HIPAA compliance exposure regarding Protected Health Information (PHI).

## Solution Overview
To remediate these structural failures, a greenfield enterprise identity infrastructure was engineered and deployed from the ground up by standing up the `NMG.com` domain on a fresh Windows Server instance. A multi-tier Organizational Unit (OU) hierarchy was designed to partition the business logically into distinct departments, including Finance, HR, IT, and Operations. Role-Based Access Control (RBAC) was systematically implemented by binding dedicated security groups to each OU, establishing strict least-privilege administrative and file-share access boundaries. Finally, 15 real corporate user identities were cleanly provisioned using rigorous data entry validation to enforce absolute consistency across SAMAccountNames, UPNs, job titles, and departmental attributes. This robust deployment successfully modernizes Northstar’s access lifecycle management, ensures immediate regulatory compliance, and provides a scalable blueprint for future network expansion.

## Video Walkthrough
*🎥 [https://www.loom.com/share/d768df7e72a04536915436e01a7b9aec]*

## Tools Used
* Windows Server 
* Active Directory Domain Services (AD DS)
* VirtualBox / Hypervisor Environment
* Group Policy Management
* GitHub (Version Control & Portfolio Architecture)
* Role-Based Access Control (RBAC) Framework

## Project Timeline
* **Day 1:** Domain creation and domain controller promotion
* **Day 2:** Organizational unit and security group design
* **Day 3:** User provisioning and RBAC implementation
* **Day 4:** Incident response and resolution (Ticket NMG-0047)
* **Day 5:** Documentation and case study packaging

## Key Accomplishments
* Built the authoritative `NMG.com` domain from scratch and verified domain controller health using directory services diagnostic utilities (`dcdiag`).
* Designed and deployed a clean, department-based Organizational Unit (OU) tree structure isolating Finance, HR, IT, and Operations business units.
* Implemented a strict Role-Based Access Control (RBAC) architecture using dedicated department security groups to enforce the principle of least privilege.
* Mass-provisioned 15 user accounts across all departments, ensuring absolute compliance with standardized naming conventions and explicit attribute parameters.
* Diagnosed and remediated a complex, multi-cause access ticket (NMG-0047) using a "Five Whys" diagnostic framework to resolve combined incorrect OU placement and missing security group memberships.
* Compiled and archived a comprehensive incident resolution and root cause analysis report to build a robust internal engineering knowledge base.

## Repository Structure
```text
├── README.md                      # Executive summary, project roadmap, and portfolio overview
├── /Documentation                 # Hard infrastructure data logs and architecture mappings
│   ├── Domain Config File         # Day 1 technical parameters (Static IP, DC name, domain specifications)
│   ├── Security Group Doc         # Day 2 structural layout mapping OUs to their business functions
│   ├── User List Documentation   # Day 3 provisioning directory of all 15 active user accounts
│   └── RBAC-Structure.md          # Clean Markdown matrix aligning business departments to access layers
├── /Incident-Reports              # Forensic security logs and compliance ticketing files
│   └── NMG-0047-Resolution.txt    # Official root-cause analysis and remediation report for Jane Cooper's account
└── /Screenshots                   # Visual evidence and validation captures of the live production environment
    ├── Day1-NMG-Domain-Created.png
    ├── Day1-Server-Manager.png
    ├── Day1-DCDiag-Results.png
    ├── Day2-OU-Structure.png
    ├── Day2-Security-Groups.png
    ├── Day3-Users-Provisioned.png
    ├── Day3-Security-Group-Memberships.png
    ├── Day3-Final-Expanded-Tree.png
    ├── Day4-Jane-Wrong-OU.png
    ├── Day4-Jane-Fixed-OU.png
    └── Day4-Jane-Fixed-GroupMembership.png
