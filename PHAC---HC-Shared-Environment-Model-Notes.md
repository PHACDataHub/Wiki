* Cant see user account ID's
  * Difficult to manage users with out having access to Admin console 
  * Cant change user emails 
  * There is an opportunity for use to manage our own users, but access needs to be granted in the admin console
    * https://support.google.com/cloudidentity/answer/2405986?hl=en
  * Currently any Google ID can be invited into a project via IAM panel
    * https://cloud.google.com/resource-manager/docs/organization-policy/restricting-domains
* Hammer out what cloud profile posture we're at.
* Issue with the current deployment of guardrails. Permissions need to be delegated to enable editing of policies. Polciies are defined at the top of the organization.
  * External IPs blocked
  * Policy for "Skip default network creation". This is causing confusion.
  * Cloud marketplace disabled
  * GCP Workstations is blocked because its not available in Canada regions
* Users are able to create projects at the root of the org, this is default behavior 
  * https://serverfault.com/questions/882599/how-to-prevent-a-user-from-creating-gcp-project
* Opportunity to implement various levels of JIT access
 *  https://cloud.google.com/architecture/manage-just-in-time-privileged-access-to-project
