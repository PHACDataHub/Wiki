# Access Policy
## Table of Contents
- [Introduction](#introduction)
- [Roles and Responsibilities](#roles-and-responsibilities)
- [Base GCP Account (all users)](#base-gcp-account-all-users)
  - [Shared Identities](#shared-identities)
  - [Password Policy](#password-policy)
- [YubiKey](#yubikey)
  - [Lost or Stolen YubiKey](#lost-or-stolen-yubikey)
- [Non-Elevated Accounts](#non-elevated-accounts)
- [Elevated Accounts](#elevated-accounts)
- [Access Reviews](#access-reviews)
- [GCP Cloud Shell / Cloud Console](#gcp-cloud-shell--cloud-console)
- [IAM Permission Mapping](#iam-permission-mapping)
- [Service accounts](#service-accounts)
- [Auditing / Logging](#auditing--logging)
## Introduction
This Access Policy establishes guidelines for managing Google Cloud Platform (GCP) accounts within our organization. It covers the creation and management of both standard and elevated accounts, emphasizing security through multi-factor authentication with YubiKey, adherence to password policies, and the principle of least privilege. Designed to maintain secure and efficient access to our cloud resources, this policy aligns with our organizational security standards and regulatory compliance, ensuring a consistent and secure approach to our GCP infrastructure management.

### Review
This policy shall be reviewed annually.

## Roles and Responsibilities
| Role | Responsibility | Additional Notes
|----------------------------------------|-----------------------|---|
| Identity Creation                      | GCP Admin at HC / DTB ||
| Elevated Account provisioning          | GCP Admin at HC / DTB ||
| GCP Account Management (IAM)           | ...                   ||
| Permission Mapping for Identities (DMIA Level) | GCP Admin at HC / DTB | HC Does mappings for things such as the infrastructure service account(s) that automate project creation, and for elevated accounts |
| Permission Mapping for Identities (Project Level)     | handled by individual project ||
| Service Account management (Project Level)            | handled by individual project ||
| Access Review                          | Both PHAC and HC | HC generates reports on account usage, and flags accounts for handling that are not being used.  If PHAC is aware of a reason to change an identity's status (i.e. user left PHAC), then HC is informed in an Administrative chat PHAC and HC share. |
| YubiKey provisioning                   | PHAC Infrastructure Team                   ||

## Base GCP Account (all users)
All users (elevated or not) that wish to use GCP must have a GCP identity created.  All users with a valid PHAC email address can request an identity for GCP.

Currently this involves making a request to HC/DTB for an account to be created.  The request is done in a “GCP Admin” chat channel in MS Teams and is actioned by HC.  They notify PHAC in the same channel when the creation is completed. This account will have no roles or permissions assigned to it at first.

The same above step is used for password resets or if an account has to be recreated due to MFA issues.

### Shared Identities
We do not allow creation of an account that is meant to be shared by multiple users.  The only exception to this is the break-glass emergency recovery accounts managed by HC

### Password Policy
All GCP identities use a password policy created at the org level of the tenant. The HC GCP team controls this. PHAC uses whatever settings HC is using.

## YubiKey
* All users brought into GCP because of a PHAC request will be issued a YubiKey to have hardware-based MFA.  Exceptions can be made in emergencies, however, a YubiKey will eventually be issued.  The user is allowed to use an Authenticator app until they receive their YubiKey.
* All YubiKeys issued are permanently issued to the user, and can be used for more than just GCP MFA.  Users are encouraged to use them for greater personal online security.  There is no returning the key to PHAC once it is issued.
* Staff provisions a security key to the user using Yubico Enterprise Delivery Portal.
* Users are encouraged to use an authenticator app as their back-up.
* We should investigate if it is possible to have SMS/Email turned off in the tenant as an option.
   * This may only be possible if we get our own org to manage in the tenant due to HC having it on for all users at the moment.
### Lost or Stolen YubiKey
* Process [doc/template is kept in SharePoint](https://022gc.sharepoint.com/:w:/s/InformationTechnology-PlanandOrganizeDMIA-GDIACDSB-DMIAD/ESotTWlhykFNjK5NNkE7324BWX6VDonwYT0EbaJiYXw1Fg?e=ALJLNf).
* Users must report a lost or stolen YubiKey as soon as possible.
*  The action taken will be to remove the YubiKey association from the user' GCP identity, and they will have to use the authentication app until a new YubiKey is issued.
* PHAC Infrastructure team will notify HC/DTB GCP team in the shared admin chat what identity needs to have the YubiKey disassociated.  HC will remove the YubiKey and notfiy PHAC in the admin channel when it is completed.
## Non-Elevated Accounts
* In Experimentation: Normal users will have Owner or Editor roles on a given project.
* In Operations:  Normal users will not have privileges to create anything.  They will likely be limited to view, or a custom role that would allow them to upload/download data to work with a system in operations (dev/test/prod).
## Elevated Accounts
* At the moment elevated accounts are created with the following format: “admin.fname.lname@gcp.hc-sc.gc.ca”
* Elevated permissions are negotiated with HC as needed.
* Future:  We intend to move to a JIT access model.  Where the elevated accounts will elevate themselves as needed for limited amounts of time.
## Access Reviews
* Accounts are currently reviewed manually by DTB. The interval is not yet known to the DE team.
* DE delegates access review to the project teams. 
* Least privilege is automatically evaluated for all accounts via IAM reccomender.
* Notification to HC/DTB of a change of status to a user's identity (i.e. they leave the Agency) is done via the group admin chat we share with them.

## GCP Cloud Shell / Cloud Console
* All users have access to the Google Cloud Shell/Console.  They are limited in what they can do by the inherent security-trimming in GCP.
## IAM Permission Mapping
* This will be handled via IaD (Infrastructure as Data) / IaC (Infrastructure as Code).  ConfigController will ensure that roles that are explicitly defined in IaD will exist and will remediate any attempted changes to roles.  
   * In the Experiment space the above rule is loosened to allow Owners of a project to explicitly add and remove users via the GCP Console.
   * In non-experiment space the only way to add/remove identities will be via IaD.  This includes Service Accounts.
## Service accounts
* Service accounts are a major part of GCP architecture.  There will be far too many to list in a document like this.
* Service accounts can be identified because they end with "gserviceaccount.com" domain.
* All service accounts start with no permissions, and thus are "least privilege" to start.
* Using the built-in logging/auditing tools all service accounts can be reviewed.
## Auditing / Logging
* All resources in GCP are subject to being logged.  
* Security Command Centre is used to view current security state.  It can be scoped in many ways as needed.
* [[GCP Logging and Audit Policy|Policy-GCP-Logging-and-Audit-Policy]]
