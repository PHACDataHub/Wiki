# Account Types and Management in Google Cloud Platform

## 1. Account Types and Their Management

Our organization utilizes a variety of accounts to administer our Google Cloud Platform (GCP) infrastructure. 

- **Individual Accounts**: These accounts are associated with identities either managed and synchronized through Azure AD or maintained directly by GCP. Roles associated with these accounts range from cloud administrators to regular cloud users.

- **Service Accounts**: Primarily used for automation and reporting, these accounts, managed by GCP, have limited access scopes and can be seen as shared accounts due to their function.

- **Emergency Accounts**: These accounts are activated during crisis situations. They have comprehensive access privileges to our GCP organization/DMIA folder.

- **Guest Accounts**: Designed for users external to our organization and not part of Azure AD, these accounts provide temporary access to our GCP environment.

Our management approach for these accounts aligns with GCP's standard practices, encompassing the lifecycle of creation, activation, modification, and removal of accounts. Each account is assigned a unique identifier to prevent any ambiguity, and we systematically ensure appropriate assignment and resetting of permissions and privileges.

## 2. Temporary and Emergency Accounts Management

Emergency accounts are used strictly during emergencies. These accounts have full access to our GCP organization/DMIA folder but are subject to extensive monitoring and logging of their activities. While we don't have specific protocols defined yet, we're working towards establishing a robust emergency account management process. 

## 3. Training Programs

We leverage training programs from Google and other third-party service providers to equip our personnel with the necessary skills to handle IAM responsibilities in GCP. This ensures the right people manage the right access, contributing to our secure and reliable infrastructure.

## 4. Roles and Responsibilities

In our organization, the responsibility for creating new GCP user accounts rests with Google Cloud Organization administrators. Initially, these accounts do not possess any permissions but exist as GCP identities. Subsequent to their creation, GCP project owners or administrators can assign access and permissions to these identities, which are selected from the standard set of GCP cloud roles.

This delineation of roles ensures that only authorized personnel can manage user accounts, thus reinforcing our security measures and aligning with the requirements of IT security.
