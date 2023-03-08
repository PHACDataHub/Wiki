* Cant see user account ID's
  * Difficult to manage users with out having access to Admin console 
  * Cant change user emails 
  * There is an opportunity for use to manage our own users, but access needs to be granted in the admin console
    * https://support.google.com/cloudidentity/answer/2405986?hl=en
* Hammer out what cloud profile posture we're at.
* Issue with the current deployment of guardrails. Permissions need to be delegated to enable editing of policies. Polciies are defined at the top of the organization.
  * External IPs blocked
  * Cloud marketplace disabled
* Users are able to create projects at the root of the org, this is default behavior 
  * https://serverfault.com/questions/882599/how-to-prevent-a-user-from-creating-gcp-project