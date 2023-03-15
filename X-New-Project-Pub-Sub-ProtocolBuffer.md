# Automation of New Project Creation Using Pub/Sub - First Thoughts

> :warning: This goes away from the model Michael has been advocating.  He has consistently talked about configConnector.  It is likely not worth investing too much energy into the thoughts below if something like configConnector `auto-magically` can create the resources. Is configConnector able to have (some of the mild) nuance suggested below (i.e. multiple projects created instead of one under a folder).

Using Pub/Sub and google cloud functions (no Internet exposure) to generate:
1. New folder to hold project(s).
2. New Project(s)
3. New Security group(s) and members. **These are created up at the root org level**
    * Groups/types used so far:
    * Owners
    * Editors
4. Attach Security group(s) to project(s).
5. Create Budget and Alert.
6. Attach to project(s)

## Questions
- If we have more than one project (i.e. dev/text/prod) do we only have one budget for all three?  This will complicate things slightly at a logic level, as opposed to one budget per project.  Not the end of the world, but a question to be answered.
- If we have dev/test/prod projects to be created, do we publish three messages, and then do tests to see if the Folder already exists? I think one message with a `google.protobuf.ListValue` (think array) that holds one or more environments to be created would be a good approach.

## Structure of custom ProtoBuff
### Definition
```
syntax = "proto3";
message ProtocolBuffer {
  string owner_gcp_account = 1;
  string project_name = 2;
  google.protobuf.ListValue environment_type = 3;
  int32 parent_folder = 4;

}
```
### Example 1
```
{
  "owner_gcp_account": "bob.mckenzie@gcp.myorg.org",
  "project_name": "ph-projectname"
  "environment_type": ["experimental"],
  "parent_folder": "23324234234"
}
```
### Example 2
```
{
  "owner_gcp_account": "bob.mckenzie@gcp.myorg.org",
  "project_name": "ph-projectname"
  "environment_type": ["development", "test", "production"],
  "parent_folder": "23324234234"
}
```
### Always more questions!
- What is the minimal payload that we can derive the rest from?
    - I.e. using the project name we can derive the project name - Folder: `ph-janedoe`, Project: `phx-janedoe`.
    - Derive security group names: `phx-janedoe-owner@gcp.hc-sc.gc.ca` or `phx-janedoe-editor@gcp.hc-sc.gc.ca`
    - Derive Budget and Billing name: `phx-janedoe-budget`
- Is this even the right approach?  A vendor showed an architecture diagram that showed things broken up across multiple Pub/Sub topics.

