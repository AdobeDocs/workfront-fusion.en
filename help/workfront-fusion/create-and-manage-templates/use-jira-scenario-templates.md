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

## Configure Workfront

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

