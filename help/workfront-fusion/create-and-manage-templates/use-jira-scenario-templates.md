---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Use templates to connect Adobe Workfront Fusion and Jira
description: Use these templates to automate workflows between Adobe Workfront Fusion and Jira.
author: Becky
feature: Workfront Fusion
---
# Use templates to connect Adobe Workfront Fusion and Jira

Adobe workfront Fusion offers templates that can automate common workflows between Fusion and Jira. 

## Access requirements

License of Jira Cloud, Workfront and Fusion.
Workfront: System Admin permissions to create users, create custom forms and custom fields.
Jira: System Admin permissions to create users, create custom fields, modify screens and modify Webhooks.
Fusion: A Team Member (at least) able to develop, test, execute, and facilitate error resolution in scenarios.

### Assumptions

* Workfront is the source of truth of the overall Marketing campaign project
* Jira is being used by technical teams, fulfilling part of a project that started in Workfront.
* Not all Jira users have access to Workfront or vice-versa. 
* Workfront and Jira are hosted in the cloud.

## Data Model (Field Mappings)

Workfront    Jira    Direction    Notes
ObjId    WF ID    WF->Jira    Upon Jira Issue Creation
Jira Key    Issue Key    Jira->WF    Upon Jira Issue Creation
Jira Link    -    Jira->WF    User Clickable link in WF to Jira
(-)    WF Link    WF->Jira    User Clickable link in Jira to WF
Name    Summary    WF->Jira    
Description    Description    WF->Jira    
Status    WF Status    WF->Jira    WF Status
Jira Status    Status    Jira->WF    Jira Status
Planned Completion Date    Due Date    WF->Jira    Planned Completion Date
Notes    Comments    WF<->Jira    Bidirectional copy
Document    Attachment    WF-> Jira    As attachments on issue creation and comments on new documents after creation.


## Configure Jira

To use these modules, the following must be created in Jira:

* A System Integration User
* Three specific custom fields

### Create a System Integration User in Jira

1. In Jira, create a specific user called System Integration User. This user should only by used by Workfront Fusion, and should not represent a human user. This user's credentials will be used by Workfront Fusion connections. 

### Create necessary custom fields in Jira

This integration expects three specific fields in the Jira account it connects to. Without these fields, the integration will be unsuccessful

1. In Jira, go to **Settings** (gear icon) and select **Work Items**.
1. In the left navigation, select **Custom fields**.
1. In the upper-right corner of the screen, click **Create custom field.**
1. Create the following fields:

   |Field name|Field type|
   |---|---|
   |WF ID|Text field (single line)|
   |WF Status|Text field (single line)|
   |WF Link|URL field|

   For information on creating links in Jira, see the Jira documentation on creating fields.
1. Add the newly created fields to the screen associated with your Jira project. 

   For information on screens in Jira, see the Jira documentation on setting up work item screens.


## Configure Workfront

To use these modules, the following must be created in Jira:

* A System Integration User
* A specific custom form

### Create a System Integration User in Workfront

1. In Workfront, create a System Integration user. This user is only used by Workfront Fusion, and does not represent a human user. Tasks assigned to this user will trigger the scenario that syncs Workfront with Jira.

   For instructions, see [Create a user]().

### Create a custom form in Workfront

1. In Workfront, begin creating a custom form. 

   For instructions, see []().
1. Name the form "**JIRA Fields**".
1. Include the following fields on the custom form:

   |Field name|Field type|
   |---|---|
   |Jira Key|Single line text field|
   |Jira URL|Single line text field|
   |JIRA status|Single line text field|

1. Add any additional fields that you will want to map between Jira and Workfront.
1. Save the custom form.

>[!NOTE]
>
>We recommend restricting this form from edits by other users. 
>
>For instructions, see []().

## List of scenarios

Eight ready-to-use templates for Jira will be available by August to help replicate common workflows and accelerate implementation. Templates are fully customizable to meet specific business needs and can be extended as requirements evolve. 

* **WF-to-Jira Initial Assignment (Tasks and Issues)** (Required)
* **Jira-to-WF Integration (Tasks and Issues)** (Required)
* WF-to-Jira Changes (Issues)
* WF-to-Jira Changes (Tasks)
* WF-to-Jira New Attachments (Tasks and Issues)
* WF-to-Jira Remove Attachments (Tasks and Issues)
* WF-to-Jira New Notes (Tasks and Issues)
* WF-to-Jira Remove Notes (Tasks and Issues)

