# Logging and Audit Policy

## Introduction
In the dynamic environment of Google Cloud Platform (GCP), robust logging and audit mechanisms are vital to safeguarding our digital assets and ensuring compliance with industry standards. This policy delineates the framework for utilizing the Security Command Centre (SCC) to monitor, log, and audit activities across our GCP projects. It is crafted to provide clear directives for the PHAC GCP infrastructure team and project owners, ensuring accountability and swift response to security and data risks. The policy also outlines the collaboration with Health Canada (HC) for comprehensive coverage and the integration of advanced monitoring tools like MS Sentinel and CCCS cloud sensors. By standardizing our approach to logging and auditing, we aim to foster a secure cloud ecosystem where infrastructure integrity and incident response readiness are paramount.

## Security Command Centre (SCC)
The Google Cloud Platform's Security Command Centre (SCC) provides an integrated solution for monitoring and responding to security and data risks across GCP projects. This documentation focuses on leveraging the SCC for comprehensive logging and auditing, which are crucial for maintaining security and compliance in cloud environments.
## Infrastructure (Org-scale)
* The PHAC GCP infrastructure team will have access to all entries in SCC within the DMIA portion of the tenant.  Health Canada is responsible for everything else.
* Additionally, HC can consume logs from within the DMIA portion of the tenant to allow a more holistic view of the current state.
* There is likely going to be a mechanism that sends some events to MS Sentinel in Azure per what HC Security wants.  This is beyond the scope of the PHAC infrastructure team to handle.
* Work is being started on incorporating CCCS cloud sensors as well.
## Infrastructure-Team Owned Template-Based Applications
Example: A template that spins up Vertex + storage bucket for a finite time for processing and is then destroyed when done.  The client owns the input and output, but not the infrastructure in this scenario.
* This is covered in the Org-scale section above.
## Custom Applications
* Individual projects will be responsible for logging in their own application (assuming a custom application of some sort).  How this works is TBD per project.
* All projects will be able to use SCC to view security-data about their applications.
## Incident Response
* [[Incident Response|Concept-Of-Operations-(ConOps)-‐-GCP#discovery-of-a-security-incident]]
