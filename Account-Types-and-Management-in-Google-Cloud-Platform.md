## Identification and Authorization of Users

In order to maintain optimal security and manageability of our Google Cloud Platform (GCP) environment, we categorize our users into various account types. Each account type is tailored to fulfill specific roles and responsibilities within our GCP infrastructure.

* Individual Accounts: These accounts are linked with identities managed by Azure AD or maintained directly by GCP. The roles associated with these accounts vary, with some assigned to cloud administrators and others to regular cloud users. Each individual account holder is granted permissions and access rights that align with their specific responsibilities. This mapping is done in a granular manner to ensure the principle of least privilege is upheld.

* Service Accounts: Service accounts are used to carry out automated processes or tasks within our GCP environment. These are not tied to individual end-users, but rather to services that require access to specific resources. Although these accounts might be considered shared due to their function, their access scope is well-defined and highly restricted to prevent any unauthorized access or misuse.

* Emergency Accounts: In the event of a crisis, emergency accounts may be activated. These accounts are given comprehensive access privileges to our GCP organization/DMIA folder. The use of these accounts is strictly regulated and only authorized during emergencies. Their usage is monitored closely to avoid any potential misuse.

* Guest Accounts: Our infrastructure occasionally hosts users who are external to our organization and not a part of Azure AD. For these users, we provide guest accounts that offer temporary access to our GCP environment. These accounts are time-limited and are strictly monitored throughout their lifecycle to ensure they are used solely for the intended purpose.

Each account type, be it individual, service, emergency, or guest, is managed diligently. Upon creation, these accounts are devoid of any permissions and exist as mere GCP identities. Only the Google Cloud Organization administrators have the authority to create and assign permissions to these accounts. Subsequent to their creation, GCP project owners or administrators assign access or permissions, selected from the standard set of GCP cloud roles, based on the specific requirements of the account holder. The permissions and access rights are reviewed periodically and updated as necessary.

This systematic and meticulous management of user identification and authorization strengthens our security posture and ensures compliance with our internal policies and regulatory requirements.

## Access Rights and Permissions

The assignment of access rights and permissions within our Google Cloud Platform (GCP) environment is a critical aspect of our security strategy. Ensuring that users only have access to the resources necessary to perform their tasks, and no more, helps to maintain the principle of least privilege and mitigates the risk of unauthorized data access or system misuse.

Our process for managing access rights and permissions is outlined below:

* Role-Based Access Control (RBAC): We employ RBAC to determine the levels of access that each user requires. The rights and permissions are determined based on the roles assigned to individual or service accounts. These roles are selected from GCP's standard set of cloud roles, providing us with a wide range of granular permissions to suit various tasks and responsibilities.

* Permission Assignment: Only Google Cloud Organization administrators have the authority to assign permissions to the accounts. This ensures a controlled and secure environment where access rights are granted by authorized personnel only. Following the creation of an account, GCP project owners or administrators can assign further access rights or permissions to these identities as needed, ensuring the account holder has the necessary access to perform their duties.

* Emergency Access: In the case of crisis situations, emergency accounts with broad access privileges may be activated. The use of these accounts is strictly controlled, and their activities are extensively monitored and logged to prevent unauthorized use.

* Temporary Access: For guest users who require temporary access to our GCP environment, time-limited guest accounts are created. These accounts are granted access rights based on the requirements of their intended purpose and are deactivated once their usage period has ended.

* Periodic Review and Updates: Access rights and permissions are not static and require regular reviews to ensure they remain appropriate for each user's current role and responsibilities. The review process involves auditing existing access rights, assessing the need for access to additional resources, and revoking unnecessary permissions.

Through these comprehensive and meticulous access rights and permissions management practices, we uphold a strong security posture and ensure compliance with IT security standards and regulatory requirements.

## Lifecycle of System Accounts

Managing the lifecycle of accounts in our Google Cloud Platform (GCP) environment is key to maintaining a secure and efficient system. Each phase of an account's lifecycle, from creation to deactivation, is monitored and controlled with due diligence.

### Account Creation

The first step in the lifecycle is the creation of the account. Only authorized Google Cloud Organization administrators can create new GCP user accounts. These accounts, upon creation, are devoid of permissions and serve as GCP identities.

### Role Assignment and Permission Granting

After an account is created, GCP project owners or administrators assign the appropriate roles and permissions. Roles are chosen from GCP's standard set of cloud roles and permissions are assigned based on the account holder's responsibilities and needs.

### Account Usage and Monitoring

Once activated and appropriately equipped with access rights, the accounts are ready for use. Throughout their active period, all account activities are logged and monitored to detect and respond to any suspicious activity promptly.

### Periodic Review of Account Privileges

Access rights and permissions are subject to regular review. This review ensures that account privileges align with the current role and responsibilities of the account holder. Unnecessary permissions are revoked, and additional permissions are granted based on the requirements.

### Account Deactivation

Accounts that are no longer needed are promptly deactivated. Conditions for deactivation include instances when shared, emergency, or temporary accounts are no longer required, or when individuals are transferred or terminated. 

By managing the lifecycle of system accounts diligently, we ensure that all accounts are used responsibly and securely, thereby enhancing our security measures and compliance with IT security standards.

## Training Requirements for Different Types of Accounts

User education is a critical aspect of managing our Google Cloud Platform (GCP) environment securely. To maintain a secure and compliant system, it is essential that users who interact with our GCP environment are equipped with the necessary knowledge and understanding of the platform.

### Individual and Service Accounts

Users managing **Individual Accounts** and **Service Accounts** are required to undergo a comprehensive training program. This includes both theoretical and practical sessions covering a wide range of topics:

- Understanding the concepts of Identity and Access Management (IAM) in GCP.
- Recognizing the importance of the principle of least privilege and how it applies to their roles.
- Learning to perform their tasks efficiently without inadvertently compromising security.
- Understanding the implication of their actions within the GCP environment.

### Emergency Accounts

Users with access to **Emergency Accounts** require additional training. This training focuses on crisis management and decision-making under pressure:

- Understanding the purpose and proper use of emergency accounts.
- Recognizing the responsibilities that come with access to emergency accounts.
- Identifying what constitutes a crisis situation warranting the use of an emergency account.
- Knowing how to act quickly and effectively in crisis situations.

### Guest Accounts

Users given access via **Guest Accounts** are typically provided with a basic introduction to the GCP environment:

- Understanding the restrictions and limited scope of access associated with guest accounts.
- Learning the proper use of the resources accessible to them.
- Recognizing the importance of respecting the boundaries set by the access limitations.

Through these tailored training programs, we ensure all users are equipped with the knowledge necessary to manage their accounts responsibly and securely, thus minimizing the risk of accidental misuse or security compromise.


## Procedures for Disabling or Deactivating Accounts

Properly managing the end stage of an account's lifecycle is crucial to maintaining the security of our Google Cloud Platform (GCP) environment. When accounts are no longer needed or if account holders leave the organization or change roles, it is essential to disable or deactivate these accounts promptly. 

Our procedures for disabling or deactivating accounts are as follows:

### Identification of Accounts for Deactivation

We continuously monitor account activity and usage. Accounts that are identified as no longer needed, such as shared, emergency, or temporary accounts, or those tied to individuals who have been transferred or terminated, are flagged for deactivation.

### Review and Approval for Deactivation

Before an account is deactivated, the account status and usage are reviewed by authorized personnel. This is to ensure that no ongoing tasks will be disrupted by the deactivation.

### Execution of Deactivation

Upon approval, the account deactivation is carried out by authorized Google Cloud Organization administrators. The deactivation process ensures that the account no longer has access to any GCP resources.

### Post-Deactivation Review

After the account deactivation, a post-action review is performed to ensure that the account has been successfully deactivated and to confirm that there are no lingering access rights or permissions.

### Record Keeping

All deactivation actions are recorded and kept for auditing purposes. This ensures a transparent and traceable process, enabling accountability and facilitating potential investigations in the future.

Through these deactivation procedures, we ensure that unnecessary accounts do not pose a security risk, thereby enhancing our overall security posture and compliance with IT security standards.
