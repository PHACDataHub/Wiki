# Logging and Audit Policy

## Table of Contents
- [Introduction](#introduction)
- [Roles and Responsibilities](#roles-and-responsibilities)
- [Audit and Logging](#audit-and-logging)
- [Monitoring and Notification of Findings](#monitoring-and-notification-of-findings)
- [Protection of Audit Information](#protection-of-audit-information)
- [Infrastructure (Org-scale)](#infrastructure-org-scale)
- [Infrastructure-Team Owned Template-Based Applications](#infrastructure-team-owned-template-based-applications)
- [Custom Applications](#custom-applications)
- [Incident Response](#incident-response)


## Review
This policy should be reviewed on an annual basis.

## Introduction
In the dynamic environment of Google Cloud Platform (GCP), robust logging and audit mechanisms are vital to safeguarding our digital assets and ensuring compliance with industry standards. This policy delineates the framework for utilizing the Security Command Centre (SCC) to monitor, log, and audit activities across our GCP projects. It is crafted to provide clear directives for the PHAC GCP infrastructure team and project owners, ensuring accountability and swift response to security and data risks. The policy also outlines the collaboration with Health Canada (HC) for comprehensive coverage and the integration of advanced monitoring tools like MS Sentinel and CCCS cloud sensors. By standardizing our approach to logging and auditing, we aim to foster a secure cloud ecosystem where infrastructure integrity and incident response readiness are paramount.

## Roles and Responsibilities

The following table outlines the key roles and their associated responsibilities within the GCP Access Policy framework. This division of responsibilities ensures clarity in the management of GCP identities, provisioning of YubiKeys, and the maintenance of our cloud infrastructure.

| Role                                             | Responsibility                                                                                      | Additional Notes                                                                                                      |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **GCP Admin at HC/DTB**                          | - Initial identity creation<br>- Password policy enforcement<br>- Elevated account provisioning      | Responsible for overarching access controls and policy enforcement within the GCP environment.                         |
| **PHAC Infrastructure Team**                     | - YubiKey provisioning<br>- Service account management                                              | Handles the distribution and management of YubiKeys and oversees service accounts at the PHAC level.                   |
| **Individual Project Teams**                     | - Permission mapping for identities<br>- Service account management<br>- Access review              | Manages project-specific access controls, reviews access privileges, and maintains service accounts within projects. All of this is IaD/IaC in operations.  |
| **HC/DTB GCP Team**                              | - Auditing and logging<br>- Incident response coordination                                          | Coordinates security measures, including logging and incident response, across the GCP infrastructure.|
| **Users**                                        | - Reporting lost or stolen YubiKeys<br>- Complying with access and authentication protocols         | Required to adhere to security protocols and promptly report any security incidents. 

## Audit and Logging
### Per security controls AU-2 - all systems will be capable of auditing the following events if applicable: 
* Successful and unsuccessful account logon events, 
* Account management events, 
* Object access, 
* Policy change, 
* Privilege functions, 
* Process tracking, 
* System events.  

For Web applications: 
* All administrator activity, 
* Authentication checks, 
* Authorization checks, 
* Data deletions, 
* Data access, 
* Data changes
* Permission changes.

### Specifically (at a minimum) all systems will be able to audit the following:
For privileged user/process events (if applicable)
* Successful and unsuccessful attempts to access, modify, or delete security objects (Security objects include audit data, system configuration files and file or users’ formal access permissions.)
* Successful and unsuccessful logon attempts
* Privileged activities or other system level access
* Starting and ending time for user access to the system
* Concurrent logons from different workstations
* All program initiations 

For unprivileged user/process events:
* Successful and unsuccessful attempts to access, modify, or delete security objects
* Successful and unsuccessful logon attempts
* Starting and ending time for user access to the system
* Concurrent logons from different workstations
## Monitoring and Notification of Findings
Monitoring frequency and notification protocols are as follows:
- Monitoring is always ongoing once SCC is enabled.  

## Protection of Audit Information
Audit information will be protected from unauthorized access and modification by the built-in security trimming in GCP. Only people with the appropriate GCP role will be able to see all logs.  Individual projects are allowed to see things associated to their project in SCC.

The PHAC administrative team is small.  All admins have the rights to view logs and audit entries in order to have enough people available for this activity when needed.

If the PHAC administration team is unavailable, and the issue cannot wait, then the HC GCP Admin team should be contacted for support.


## Security Command Centre (SCC)
The Google Cloud Platform's Security Command Centre (SCC) provides an integrated solution for monitoring and responding to security and data risks across GCP projects. This documentation focuses on leveraging the SCC for comprehensive logging and auditing, which are crucial for maintaining security and compliance in cloud environments.
## Infrastructure (Org-scale)
* For Security events, HC GCP is RESPONSIBLE and ACCOUNTABLE, while the DMIA Infrastructure team is to be CONSULTED and INFORMED (in RACI terms).
* HC GCP will ensure an appropriate level of monitoring to communicate timely information on security events.
* If a security incident occurs which directly impacts DMIA related work, the DMIA team is CONSULTED prior to and INFORMED about actions being taken. DMIA will liaise with the client project owners to ensure issues are addressed, if needed. => This last point is a level of RESPONSIBLE for the local task which is important but different from the overarching R mentioned above.

## Infrastructure-Team Owned Template-Based Applications
Example: A template that spins up Vertex + storage bucket for a finite time for processing and is then destroyed when done.  The client owns the input and output, but not the infrastructure in this scenario.
* This is covered in the Org-scale section above.
## Custom Applications
* Individual projects will be responsible for logging in their own application (assuming a custom application of some sort).  How this works is TBD per project.
* All projects will be able to use SCC to view security-data about their applications.
* The ability to view SCC entries for a given project is built into the normal permission structure for projects.  This also aligns with PHAC's desire to empower projects to be more responsible for their own products (where applicable).
## Incident Response
* [[Incident Response|Concept-Of-Operations-(ConOps)-‐-GCP#discovery-of-a-security-incident]]
