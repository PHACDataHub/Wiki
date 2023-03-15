
> :warning: I am creating this as an X-file just to get these steps down someplace.  This markdown file can go away once we have established appropriate scripts.

### Simple Legend
- GCP Identity credentials must exist before the steps below.
- \<SOMETHING\> = Replace with a string.
- $CAPITALIZED_WORDS = environment variable (Linux)
- \\ = extends shell command to the next line in terminal.

### Overview of steps

1. Create Folder
```
gcloud resource-manager folders create --display-name=<NEW_FOLDER_NAME> \
--folder=$PHAC_ROOT_FOLDER_ID
```
2. Create Project
```
gcloud projects create <PROJECT_ID> --folder=$PHAC_ROOT_FOLDER_ID
```
3. Add Billing ID to project
> :exclamation: This was provided by Google after I noticed there was no CLI mention in the documentation page for linking project and billing account.  At some point the `beta` in the CLI below will likely not be needed.
```
gcloud beta billing projects link <PROJECT_ID> \
--billing-account=$PHAC_BILLING_ID
```
4. Create Security Group
```
gcloud identity groups create <GROUP_EMAIL> --organization=$ORG_ROOT_ID \
--group-type="security"
```
5. Add Member to Group
```
gcloud identity groups memberships add --group-email=<GROUP_EMAIL> \
--member-email=<OWNER_EMAIL> 
```
6. Attach Group to Project with Owner Role
```
@TODO ADD CLI CODE HERE
```
7. Create Budget and Alert
> :exclamation: **NOTE:**  The billing ID must be attached to the project before this is run.  It will fail otherwise.
```
gcloud billing budgets create --billing-account=$PHAC_BILLING_ID \
--display-name=<PROJECT_NAME>-budget --budget-amount=2000.00 \
--filter-projects=projects/<PROJECT_NAME> --threshold-rule=percent=0.50 \
--threshold-rule=percent=0.9 --threshold-rule=percent=1.0 \
--calendar-period=year
```
8. If a folder needs multiple environments, then steps 3 - 7 will be repeated for each environment. I.e. Dev/Test/Prod
9. Send email to user welcoming to GCP.

> :warning: As of this writing, the real focus of the above actions are to generate EXPERIMENTAL project spaces.  We will need to flesh out and make changes as we onboard more environment types.  Should the division be Exp/Test/Dev/Prod, or UCLL/PBMM?



