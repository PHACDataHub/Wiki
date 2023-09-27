# Concept of Operations (ConOps) - Data Enablement project base

## Purpose of the System
The DMIA Google Cloud account is used to provide data infrastructure and access to Googles first-party SaaS offerings to support the epidemiological and public health work of the agency.

All work in Google Cloud is done within the context of an isolated project. These projects are provisioned by members of the Data Enablement team within DMIA upon request from users within the agency.

Users access the project using mandatory MFA, and work with data up to and including Protected B. 

This evaluation assumes only that CCCS assessed services are used within the project boundary and that data above Protected B will not be used. These are terms of use for the DMIA cloud.

## Business Requirements
Rapid provisioning of isolated cloud environments for collaborative data work to support the agencies response mandate.

Granular isolation to reduce risk while supporting the agencies core business of data aggregation which involve processing of untrusted inputs

User access to cloud infrastructure access to support data science, machine learning and scientific use cases

Control over intermediary devices to support the high availability and scalability needs for the agencies data service strategy

Support for a variety of project specific usage patterns (IaaS, PaaS, FaaS, DBaaS, SaaS)

## Scope
The “project” is the basic security boundary on the Google Cloud Platform (GCP). This assessment covers the project itself, but user created resources within a project are out of scope and will be covered in separate assessments.

## Background
Each project in Google Cloud comes with an isolated VPC (Virtual Private Cloud) and firewall by default and IAM roles scoped to the project level, and for many years Google’s advice reflected what the design and naming of this security boundary suggested, that you should have “one application per project per environment.”

From their [2021 documentation](https://web.archive.org/web/20210411004021/https://cloud.google.com/docs/enterprise/best-practices-for-enterprise-organizations) explains “if you have two applications, "app1" and "app2", each with a development and production environment, you will have four projects: app1-dev, app1-prod, app2-dev, app2-prod. This isolates the environments from each other, so changes to the development project do not accidentally impact production and gives you better access control.”

DMIA’s strategy is oriented towards exactly the isolation they are describing, and this evaluation is aimed at describing the boundary, how it is created, what accounts and permissions affecting it are created and the visibility of what is inside.

## Architecture Overview
The DMIA cloud is a folder within a DTB controlled cloud account. 

![Folder Structure](https://github.com/PHACDataHub/Wiki/assets/3381709/d92e3459-e893-477a-81c0-05df3274f3ad)

Inside the DMIA folder, projects are categorized into subfolders.

![Folder Heirarchy](https://github.com/PHACDataHub/Wiki/assets/3381709/aeb46bce-e1cb-42b7-95c3-a1467290cc65)

Additional folder structure will be built out as needed.  The “ConfigConnector Core Infra Project” in the image below is under the Services folder.  This project is the project that automates initial project creation and any default infrastructure that will come with a project (i.e. monitoring, etc.).

![Simple Infrastructure Architecture](https://github.com/PHACDataHub/Wiki/assets/3381709/819ce762-e13f-45c6-93b3-df2b8e1addd2)

## Security Categorization
As described in the accompanying Statement of Sensitivity, projects created within the DMIA folder can contain data that ranges from unclassified up to and including Protected B.

This boundary safeguards data classified as Protected B from potential threats and unauthorized access. 
In the context of Google Cloud Projects, each project is an isolated workspace with its own set of resources, including data storage, application engines, and user identities. It serves to group resources that are used together for a specific task or a group of related tasks. It is an environment that is distinct from other projects, and access controls can be set up to carefully manage who has access to what within this project. 

The security concept emphasizes the principle of least privilege, ensuring that each user or service has only the permissions it needs to perform its tasks, and no more. Google Cloud Project's inherent design promotes security through compartmentalization, reducing potential vulnerabilities by separating different functionalities and data. 

The IT (Information Technology) system operation under this security concept therefore implies that all interactions with the Protected B data happen within this controlled environment, ensuring an elevated level of data protection and risk mitigation.

## Security ConOps
This section details the relevant security operations of the GCP project base:

**Google Cloud Project**: The GCP is the fundamental building block of Google Cloud Platform. It is an organized unit of work, housing and managing the resources necessary for an application. Each Google Cloud Project creates a security boundary, encapsulating the data and services within it.

**Identity and Access Management (IAM)**: Google IAM accounts are provisioned by DTB staff upon request by DE staff and have no permissions assigned by default. DE staff allow IAM accounts access to projects based on user need.

**Resource Isolation and Intercommunication**: Each GCP project is an isolated environment, meaning the resources of one project are kept separate from others, limiting potential for cross-project vulnerabilities. Data sharing between projects will be done in accordance with the TBS Enterprise Architecture Framework which requires services expose APIs for interoperability.  This approach ensures controlled inter-project interactions and helps maintain the integrity of each project's data, reducing the surface area for potential threats.

**Data Protection**: All data within the GCP is encrypted at rest by default with no customer action required. Encryption in transit is enforced for all data outside Google’s physical security boundary, and CCCS has evaluated the security of the Google Cloud Platform as appropriate for Protected B. Additional measures will be applied as appropriate at the project level.

**Monitoring and Auditing**: All logs from services running within GCP projects are visible at the organization level and will be monitored by DMIA staff with that access. Google provides several tools for real-time monitoring and logging, like Google Cloud Audit Logs and Google Cloud Monitoring. These allow for continuous oversight of the system's health and activity, identifying and alerting about potential security threats.

**Security Compliance**: GCP's security infrastructure is compliant with major certifications and regulations, ensuring it aligns with the best practices and requirements set forth by established standards.

**Incident Response and Recovery**: In the event of a security incident, GCP offers tools and features that enable swift detection, response, and recovery, minimizing potential impact.
Continuous Improvement: Google Cloud's Security Command Center provides insights and analytics, enabling IT teams to continually improve their security posture by identifying potential vulnerabilities and taking proactive measures to eliminate them.

## Sdf
Google Cloud Projects will be leveraged to form a security boundary around the Protected B data it processes and stores, utilizing GCP's robust security features to maintain the highest level of protection and integrity for the data.

## Access (Non-Elevated Accounts)
@TODO Blurb on access and identity management (offboarding?) JF has raised the want/need to verify clearance for new users to be at least reliability… How does this play when we are bringing guests into the tenant for rapid response things?  How does OICD sit in this?

Current PHAC access management policy: [[GCP Access Policy|Policy-GCP-Access-Policy]]

## Monitoring
Security relevant logs and metrics are automatically and transparently channelled to the Google’s centralized Security Command Center (SCC) service. DMIA staff have “Reader” access to SCC at the organization level, allowing them a view across all projects without needing to compromise the integrity of the “project” security boundary.

## Incident response
POSITION | RESPONSIBILITY
---------|---------
 HC/PHAC IT Security | Assess the magnitude of the security issue and respond as per procedures based on the severity of the incident.  <br><br>Respond to the generic Data Science email account (<datascience-sciencededonnees@phac-aspc.gc.ca>) if any action is being taken from a security perspective, if action should be taken by the ITAP Business Owners or administrators. <br><br>Actively work with the ITAP teams until incident is resolved and steps taken to mitigate a recurrence.
 PHAC System administrator(s) | Give the security _incident_ the time and focus it needs to resolve, govern and document.<br><br>Lead the activities to address the security incident document, review history, if a recurrence, communicate to appropriate groups, report updates, timeframes, status, resolution, lessons learned, actions taken to reduce / eliminate a recurrence.
GCP administrator(s)|Informed to be aware of incident and take actions to avoid the same or similar security incidents.  
PHAC Business Owner|Informed to be aware of incident and take actions to avoid the same or similar security incident.  

## Pre-requisites
* Training must be provided appropriate to the role and level of access.
* System administrators must be cleared to the appropriate security level.
## Assumptions
* All personnel credentials will be verified, and security clearances confirmed, prior to being granted access to the system, and that the security clearance is commensurate with the level required to perform the assigned role.  Secret clearances are required for roles with elevated privileges.
* Sufficient resources will be available to maintain the system in accordance with this policy and the activities defined within.
## Discovery of a Security Incident
* Determine severity
* Take appropriate action 
* Call IT Sec, National Security Operations Center (NSOC)
   * Unusual or adverse activity could be the first sign of a security incident. To report IT Security incidences, please contact the National Security Operations Centre (NSOC)
   * For urgent matters: NSOC hotline at 613-957-1010 (NCR) or 1-888-333-6511 (regions)
   * For non-urgent matters: NSOC email at: hc.securityopscenter-centreopssecurite.sc@hc-sc.gc.ca or use the desktop Service Gateway icon to access IT/IM services online.
* Invoke contact callout list
* HC/PHAC IT Security: itsecurity-tisecurite@hc-sc.gc.ca
* PHAC System administrator(s): john.bain@phac-aspc.gc.ca, keith.young@phac-aspc.gc.ca, michael.williamson@phac-aspc.gc.ca
* PHAC Business Owner: Data Management, Innovation and Analytics tim.allardyce@phac-aspc.gc.ca
* Initiate corrective actions as determined by NSOC, DTB IT Security or other applicable GC governing body (CSE/RCMP, CCCS (Canadian Centre for Cyber Security), etc.)
* In the event of an information spill, contact DTB IT Security and the NSOC immediately and initiate a recovery process 
## Post Incident Recovery
* Complete and forward report the product Owner
* Provide education as required to minimize further occurrences
## Identification and Authentication
* Accounts in the Google Cloud platform are currently manually created by staff on the DTB Google Cloud Platform team upon request from DMIA.
* Users logging in with these accounts are authenticated through Google’s native IAM controls. 
* By default, these accounts are simply identities, and have no permissions assigned.
* DMIA staff are responsible for assigning these identities appropriate roles on relevant projects.
* Members of the project team given the “Owner” role may add other users as required but cannot grant access outside the boundaries of that project.
* Administrator accounts require Multi-factor Authentication (MFA), the mode of which is determined by the user. The options are Duo Factor Authentication, Time-Based One-Time Password, or One Time Authentication SMS code.

