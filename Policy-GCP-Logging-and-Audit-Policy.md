# Logging and Audit Policy

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
* @TODO:  Didn't we identify this somewhere else?
