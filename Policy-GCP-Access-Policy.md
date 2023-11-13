# Access Policy

## Base GCP Account (all users)
All users (elevated or not) must have a GCP identity created.

Currently this involves making a request for an account to be created.  The request is done in a “GCP Admin” chat channel in MS Teams and is actioned by HC.  They notify PHAC in the same channel when the creation is completed. This account will have no roles or permissions assigned to it at first.

The same above step is used for password resets or if an account has to be recreated due to MFA issues.

## YubiKey
* All PHAC users that have GCP identities will be issued a YubiKey to have hardware-based MFA.
* Staff provisions a security key to the user using Yubico Enterprise Delivery Portal.
* Users are encouraged to use an authenticator app as their back-up.
* We should investigate if it is possible to have SMS/Email turned off in the tenant as an option.
   * This may only be possible if we get our own org to manage in the tenant due to HC having it on for all users at the moment.
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

## GCP Cloud Shell / Cloud Console
* All users have access to the Google Cloud Shell/Console.  They are limited in what they can do by the inherent security-trimming in GCP.
## IAM Permission Mapping
* This will be handled via IaD (Infrastructure as Data) / IaC (Infrastructure as Code).  ConfigController will ensure that roles that are explicitly defined in IaD will exist and will remediate any attempted changes to roles.  
   * In the Experiment space the above rule is loosened to allow Owners of a project to explicitly add and remove users via the GCP Console.
   * In non-experiment space the only way to add/remove identities will be via IaD.  This includes Service Accounts.
## Service accounts
Should scoping matter for what service account names are in this table?  (I.e. does it make sense for the alphadns SA (Service Account) to be in this table if it is only scoped to the alphadns project? I would say it does not need to be here) ….


Infrastructure Service Account Name | Role(s) | Mapping/Notes
----------|----------|---------
sccslackXXXXXX-sa@phx-projid.iam.gserviceaccount.com|Security Centre Admin|This account will be replaced with a new one once the experiment is proven.<br><br>Mapped at DMIA folder.<br><br>Used to send alerts to Slack
service-xxxxxxxxxxx@gcp-sa-yakima.iam.gserviceaccount.com|Folder Creator<br><br>Folder Editor<br><br>Project Billing Manager<br><br>Project Creator<br><br>Project Deleter|Mapped at DMIA folder<br><br>GCP-created account that creates our infrastructure.<br><br>Going to work with Chris Carty to see about us replacing this with one named/defined by us.
The JIT account needs to go here| |This will either be mapped at the DMIA folder, or near the org root depending on implementation (if HC wants to use it as well) ...
Should the alphadns SA (Service Account) go here?| | 

## Auditing / Logging
* All resources in GCP are subject to being logged.  
* Security Command Centre is used to view current security state.  It can be scoped in many ways as needed.
* @TODO: What alerts are needed?
