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

+++ Expand to view access requirements for the functionality in this article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any Adobe Workfront Workflow package and any Adobe Workfront Automation and Integration package</p><p>Workfront Ultimate</p><p>Workfront Prime and Select packages, with an additional purchase of Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront licenses</td> 
   <td> <p>Standard</p><p>Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Workfront: If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</p><p>Jira: You must have a license to Jira Cloud</p>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Access level configurations</td> 
   <td> <p>Workfront: permission to create users, custom forms, and custom fields.</p> <p>Jira: Permissions to create users and custom fields, and to modify screens and webhooks.</td> 
  </tr> 
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisites

### Workfront

* You must have a technical account on the Adobe Developer Console.

   For information and instructions, see [Technical account setup](https://developer.adobe.com/cloud-storage/guides/getting-started/technical-account-setup) in the Adobe documentation.
* You must apply System Administrator permissions to the technical account in the Adobe Admin Console Product Profiles area.

   For information and instructions, see [Create system administrators in Workfront with the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console#create-system-administrators-in-workfront-with-the-adobe-admin-console)

### Jira 

If you are using OAuth2 authorization for Jira (recommended), you must set up an OAuth2 application at [https://developer.atlassian.com/console](https://developer.atlassian.com/console). For information and instructions, see the Jira documentation.

When configuring this application, you will need the following scopes:

* `read:jira-work` 
* `read:jira-user`
* `write:jira-work`

## Assumptions

These modules assume the following:

* Workfront is the source of truth of the overall Marketing campaign project
* Jira is being used by technical teams, fulfilling part of a project that started in Workfront.
* Not all Jira users have access to Workfront or vice-versa. 
* Workfront and Jira are hosted in the cloud.

## Data Model (Field Mappings)


| Workfront | Jira | Direction | Notes |
| --- | --- | --- | --- |
| ObjId | WF ID * | WF &rarr; Jira | Upon Jira Issue Creation |
| Jira Key * | Issue Key | Jira &rarr; WF | Upon Jira Issue Creation |
| Jira URL * | - | Jira &rarr; WF | User Clickable link in WF to Jira |
| - | WF Link * | WF &rarr; Jira | User Clickable link in Jira to WF |
| Name | Summary | WF &rarr; Jira | |
| Description | Description | WF &rarr; Jira | |
| Status | WF Status | WF &rarr; Jira | WF Status |
| Jira Status * | Status | Jira &rarr; WF | Jira Status |
| Planned Completion Date | Due Date | WF &rarr; Jira | Planned Completion Date |
| Notes | Comments | WF &harr; Jira | Bidirectional copy |
| Document | Attachment | WF &rarr; Jira | As attachments on issue creation and comments on new documents after creation. |

\* These fields are configured as part of this integration setup. For instructions, see [Configure prerequisites in Workfront, Jira, and Workfront Fusion](/help/workfront-fusion/create-and-manage-templates/use-jira-scenario-templates.md#configure-prerequisites-in-workfront-jira-and-workfront-fusion).

## Configure prerequisites in Workfront, Jira, and Workfront Fusion

To use the Jira integration templates, you must perform the following configurations:

* [Configure Jira](#configure-jira)
* [Configure Workfront](#configure-workfront)
* [Configure connections in Workfront Fusion](#configure-connections-in-workfront-fusion)

### Configure Jira

To use these modules, the following must be created in Jira:

* A System Integration User
* Three specific custom fields

#### Create a System Integration User in Jira

1. In Jira, create a specific user called System Integration User. This user should only by used by Workfront Fusion, and should not represent a human user. This user's credentials will be used by Workfront Fusion connections. 

#### Create necessary custom fields in Jira

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


### Configure Workfront

To use these modules, the following must be created in Workfront:

* A System Integration User
* A specific custom form

#### Create a System Integration User in Workfront

1. In Workfront, create a System Integration user. This user is only used by Workfront Fusion, and does not represent a human user. Tasks assigned to this user will trigger the scenario that syncs Workfront with Jira.

   For instructions, see [Add users](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/add-users) in the Workfront documentation.

#### Create a custom form in Workfront

1. In Workfront, begin creating a custom form. 

   For instructions, see [Create a custom form](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/design-a-form/design-a-form) in the Workfront documentation.
1. Name the form "**JIRA Fields**".
1. Include the following fields on the custom form:

   |Field name|Field type|
   |---|---|
   |Jira Key|Single line text field|
   |Jira URL|Single line text field|
   |Jira status|Single line text field|

1. Add any additional fields that you will want to map between Jira and Workfront.
1. Save the custom form.

>[!NOTE]
>
>We recommend restricting this form from edits by other users. You can accomplish this by ensuring that any users added to the custom form have View access only. 
>
>For instructions, see [Share a custom form](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/manage-custom-forms/share-access-to-a-custom-form) in the Workfront documentation.

### Configure connections in Workfront Fusion

You must have created the System Integration users in Jira and Workfront before you can create connections.

When creating these connections, be sure to use the credentials of the created System Integration users.

If desired, you can create these connections as part of configuring the templates.

* For instructions on creating a connection to Workfront, see [Connect Workfront to Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#connect-workfront-to-workfront-fusion) in the article Workfront modules.
* For instructions on creating a connection to Jira Cloud, see [Connect Jira Cloud to Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md#connect-jira-cloud-to-workfront-fusion) in the article Jira Software modules.


## Scenarios

Eight ready-to-use templates for Jira are to help replicate common workflows and accelerate implementation. Templates are fully customizable to meet specific business needs and can be extended as requirements evolve. 

You do not need to implement all scenarios. The minimal implementation would require Scenario 1, which would create a single-direction integration to a JIRA issue from an assignment in Workfront.  You can add the additional scenarios to add robustness and more bidirectional interconnectivity between Workfront and JIRA.  You can also create additional scenarios to handle cases such as project to epic integration or JIRA issue to Workfront issue or tasks.  

Any use of these templates or extensions of these templates is considered custom configuration, and we recommend utilizing Adobe Professional Services or an Adobe partner for support and implementation. 

* **[Workfront to Jira: Create JIRA issue from Workfront task or issue assignment](#scenario-1-workfront-to-jira-create-jira-issue-from-workfront-task-or-issue-assignment)** 
* [JIRA to Workfront: JIRA to Workfront: Send updates on issues and comments back to Workfront from Jira](#scenario-2-jira-to-workfront-send-updates-on-issues-and-comments-back-to-workfront-from-jira)
* [Workfront to Jira: Changes to Workfront task to JIRA issue](#scenario-3-workfront-to-jira-changes-to-workfront-task-to-jira-issue)
* Workfront to Jira: Changes to Workfront issue to JIRA issue
* Workfront to Jira: Create comment in JIRA when new note on Workfront task or issue
* Workfront to Jira: Create comment in JIRA on deleted note on Workfront task or issue
* Workfront to Jira: Create comment in JIRA when new document on Workfront task or issue
* Workfront to Jira: Create comment in JIRA on deleted document on Workfront task or issue

### General parameters

When configuring these templates, use the following general parameters:

* **JiraBaseURL**: The base url for the Jira instance. Example: `https://myjira.atlassian.net/`
* **wfBaseURL**: The base url for the Workfront instance.  Usually: `https://<domain>.my.workfront.com` where `<domain>` is your particular Workfront domain name.
* **defaultJIRAReporterID**: The ID for the user in JIRA that creates issues. (Example: `557058:5aedf933-2312-40bc-b328-0c21314167f0`)
   You can get this ID by doing one of the following:
   * Click on the profile of the user in JIRA and check the URL in your browser. 
(Example`https://myjira.atlassian.net/jira/people/<JiraUserID>`)
   * Run the following API call on your JIRA instance to get the ID for the specific Account in JIRA: 
`GET /rest/api/3/user/search?query=email@example.com`

<!--
 
### Scenario 1: Workfront to Jira: Create JIRA issue from Workfront task or issue assignment

This scenario creates a Jira issue when a Workfront Task or Issue is assigned to the System Integration User. The scenario fill in the Summary, Description, Due Date, WF Status and WF ID fields. After the  issue is created, this scenario also uploads the list of attachments and the history of notes related to the original task or issue in Workfront.

If a Workfront task is assigned, the issue in Jira is a Task. If a Workfront Issue is assigned, the Jira issue is a Bug.

+++**Expand to view instructions for configuring Scenario 1:Workfront to Jira: Create JIRA issue from Workfront task or issue assignment**

#### Configure the trigger module

1. Click the **Templates** tab ![Templates icon](assets/templates-icon.png) in the left navigation panel.
1. Search for the template by using the search bar near the upper-left corner of the screen. You can search by template name or included applications.
1. Click the **Workfront to Jira: Create JIRA issue from Workfront task or issue assignment** template.
 
   A view of the template opens, showing information and an animation of data flow.
1. In the first module, begin adding a webhook.
1. Select the Workfront connection that you created in [Configure connections in Workfront Fusion](#configure-connections-in-workfront-fusion). 
1. In the **Record Type** field, select `Assignment`.
1. In the **State** field, select `New state`.
1. Configure the filter with the following operations, using the **And** option:

   |Field|Operator|Value|
   |---|---|---|
   |assignedToID|Equals|Enter the Workfront ID of the System Integration user|
   |TaskID |Exists||
   | projectID |Equals|Enter the ID of the project or projects that you want the webhook to watch.|

1. Enable the **Exclude updates made by this connection** option.
1. Click **Save** to save the webhook, then click **OK** to save the trigger module.
1. Continue to [Connect template modules to Workfront and Jira]()

#### Connect template modules to Workfront and Jira

1. In **each** Workfront module, in the Connection field, select the Workfront connection that you created in [Configure connections in Workfront Fusion](#configure-connections-in-workfront-fusion), then click **OK** to save the connection to that module.
1. In **each** Jira module, in the Connection field, select the Workfront connection that you created in [Configure connections in Workfront Fusion](#configure-connections-in-workfront-fusion), then click **OK** to save the connection to that module. 
1. Continue to [Update the General Parameters module](#update-the-general-parameters-module).

#### Update the General Parameters module

1. In the second module of the template (Set Environment Details), for each of the following variables, click **Add item** and enter the variable's name and value

   |Variable name | Variable value|
   |---|---|
   |defaultJiraReporterID|This is the ID of the default user when the Creator User doesn't exist in Jira. You can find this user ID by clicking on the profile of the user and checking the URL of the browser. Example: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   |JiraBaseURL| The base URL of the Jira account you are connecting to.|
   |wfBaseURL| The base URL of the Workfront account you are connecting to.|

1. Continue to [Map custom fields in Jira]()

#### Map custom fields in Jira. 

Awaiting feedback-->

+++

### Scenario 2: JIRA to Workfront: Send updates on issues and comments back to Workfront from Jira

This scenario creates a Workfront task or issue when an issue is created in Jira.

>[!NOTE]
>
>This scenario requires an OAuth2 connection for Jira. 
>If you are using OAuth2 authorization for Jira (recommended), you must set up an OAuth2 application at [https://developer.atlassian.com/console](https://developer.atlassian.com/console). For information and instructions, see the Jira documentation.

+++**Expand to view instructions for configuring Scenario 2: JIRA to Workfront: Send updates on issues and comments back to Workfront from Jira**



1. Click the **Templates** tab ![Templates icon](assets/templates-icon.png) in the left navigation panel.
1. Search for the template by using the search bar near the upper-left corner of the screen. You can search by template name or included applications.
1. Click the **Part 2: JIRA to Workfront: Send updates on issues and comments back to Workfront from Jira** template.
 
   A view of the template opens, showing information and an animation of data flow.
1. In the first module, begin adding a webhook.
1. Select a connection that uses the credentials for the System Integration user, or create a connection to Jira with the System Integration credentials.

   For instructions on creating a connection to Jira Cloud, see [Connect Jira Cloud to Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md#connect-jira-cloud-to-workfront-fusion) in the article Jira Software modules.'

1. Configure the webhook filter 

1. Continue to [Configure a webhook in Jira](#configure-a-webhook-in-jira)

#### Configure a webhook in Jira

1. In Jira, create a webhook.

   For instructions see the information on webhooks in the Jira documentation.

1. When configuring the webhook, use the following values:
 
   * **JQL**: project = "yourProjectName" (where yourProjectName = your JIRA project's name)
   * **Issue**: created, updated
   * **Comment**: created, deleted


1. Continue to [Connect template modules to Workfront and Jira (Module 2)](#connect-template-modules-to-workfront-and-jira-module-2)

#### Connect template modules to Workfront and Jira (Module 2)

1. In **each** Workfront module, in the Connection field, select the Workfront connection that you created in [Configure connections in Workfront Fusion](#configure-connections-in-workfront-fusion), then click **OK** to save the connection to that module.
1. In **each** Jira module, in the Connection field, select the Workfront connection that you created in [Configure connections in Workfront Fusion](#configure-connections-in-workfront-fusion), then click **OK** to save the connection to that module. 
<!--#### Map custom fields-->

+++

### Scenario 3: Workfront to Jira: Changes to Workfront task to JIRA issue

+++**Expand to view instructions for configuring Scenario 3: WF-to-Jira Changes (Tasks)**

1. Click the **Templates** tab ![Templates icon](assets/templates-icon.png) in the left navigation panel.
1. Search for the template by using the search bar near the upper-left corner of the screen. You can search by template name or included applications.
1. Click the **Part 3: Workfront to Jira: Changes to Workfront task to JIRA issue** template.
 
   A view of the template opens, showing information and an animation of data flow.

1. Click the template to enter the editor.
1. Select the organization and team that will own this scenario.
1. In the first module, begin adding a webhook.
1. In the Connection field, select the Workfront connection that uses the System Integration credentials.
1. In the **Record Type** field, select `Task`.
1. In the **State** field, select `New state`.
1. Configure the filter with the following operations, using the **And** option:

   |Field|Operator|Value|
   |---|---|---|
   |assignedToID|Equals|Enter the Workfront ID of the System Integration user|
   |projectID|Equals|Enter the ID of the project or projects that you want the webhook to watch.|
   |DE: Jira Key|Exists||

1. Enable the **Exclude updates made by this connection** option.
1. In the **Record Origin** field, select `Updated record only`.
1. Click **Save** to save the webhook, then click **OK** to save the trigger module.
1. In the second module, set the following variables, then click **OK** to save the module.

   |Variable name|Variable value|
   |---|---|
   |defaultJiraReporterID|This is the ID of the default user when the Creator User doesn't exist in Jira. You can find this user ID by clicking on the profile of the user and checking the URL of the browser. Example: `https://myjira.atlassian.net/jira/people/<JiraUserID>`|
   |JiraBaseURL|The base URL of the Jira account you are connecting to.|
   |wfBaseURL|The base URL of the Workfront account you are connecting to.|

1. In **each** Workfront module, in the Connection field, select the Workfront connection that uses the System Integration credentials, then click **OK** to save the module.
1. In **each** Jira module, in the Connection field, select the Jira connection that uses the System Integration credentials, then click **OK** to save the module.


+++



### Scenario 4: Workfront to Jira: Changes to Workfront issue to JIRA issue

This scenario sends updates from Workfront issues to previously connected JIRA issues.

+++**Expand to view instructions for configuring Scenario 4: WF-to-Jira Changes (Issues)**

1. Click the **Templates** tab ![Templates icon](assets/templates-icon.png) in the left navigation panel.
1. Search for the template by using the search bar near the upper-left corner of the screen. You can search by template name or included applications.
1. Click the **Scenario 4: WF-to-Jira Changes (Issues)** template.
 
   A view of the template opens, showing information and an animation of data flow.

1. Click the template to enter the editor.
1. Select the organization and team that will own this scenario.
1. In the first module, begin adding a webhook.
1. In the Connection field, select the Workfront connection that uses the System Integration credentials.
1. In the **Record Type** field, select `??`.
1. In the **State** field, select `New state`.
1. Configure the filter with the following operations, using the **And** option:

   |Field|Operator|Value|
   |---|---|---|
   |(Updates on issues)||| 
   |assignedToID|Equals|Enter the Workfront ID of the System Integration user|
   |projectID|Equals|Enter the ID of the project or projects that you want the webhook to watch.|
   |WF ID|Exists||

1. Enable the **Exclude updates made by this connection** option.
1. Click **Save** to save the webhook, then click **OK** to save the trigger module.
1. In the second module, set the following variables, then click **OK** to save the module.

   |Variable name|Variable value|
   |---|---|
   |defaultJiraReporterID|This is the ID of the default user when the Creator User doesn't exist in Jira. You can find this user ID by clicking on the profile of the user and checking the URL of the browser. Example: `https://myjira.atlassian.net/jira/people/<JiraUserID>`|
   |JiraBaseURL|The base URL of the Jira account you are connecting to.|
   |wfBaseURL|The base URL of the Workfront account you are connecting to.|

1. In **each** Workfront module, in the Connection field, select the Workfront connection that uses the System Integration credentials, then click **OK** to save the module.
1. In **each** Jira module, in the Connection field, select the Jira connection that uses the System Integration credentials, then click **OK** to save the module.


+++



### Scenario 5: WF-to-Jira New notes (Tasks and Issues)

+++**Expand to view instructions for configuring Scenario 5: WF-to-Jira New notes (Tasks and Issues)**

1. Click the **Templates** tab ![Templates icon](assets/templates-icon.png) in the left navigation panel.
1. Search for the template by using the search bar near the upper-left corner of the screen. You can search by template name or included applications.
1. Click the **Scenario 5: WF-to-Jira New notes (Tasks and Issues)** template.
 
   A view of the template opens, showing information and an animation of data flow.
1. In the first module, begin adding a webhook.
1. In the Connection field, select the Workfront connection that uses the System Integration credentials.
1. In the **Record Type** field, select `??`.
1. In the **State** field, select `New state`.
1. Configure the filter with the following operations, using the **And** option:

   |Field|Operator|Value|
   |---|---|---|
   |(Create and Updates on Notes.)||| 
   |assignedToID|Equals|Enter the Workfront ID of the System Integration user|
   |projectID|Equals|Enter the ID of the project or projects that you want the webhook to watch.|

1. Enable the **Exclude updates made by this connection** option.
1. Click **Save** to save the webhook, then click **OK** to save the trigger module.
1. In the second module, set the following variables, then click **OK** to save the module.

   |Variable name|Variable value|
   |---|---|
   |defaultJiraReporterID|This is the ID of the default user when the Creator User doesn't exist in Jira. You can find this user ID by clicking on the profile of the user and checking the URL of the browser. Example: `https://myjira.atlassian.net/jira/people/<JiraUserID>`|
   |JiraBaseURL|The base URL of the Jira account you are connecting to.|
   |wfBaseURL|The base URL of the Workfront account you are connecting to.|

1. Enable the **Exclude updates made by this connection** option.
1. Click **Save** to save the webhook, then click **OK** to save the trigger module.
1. In **each** Workfront module, in the Connection field, select the Workfront connection that uses the System Integration credentials, then click **OK** to save the module.
1. In **each** Jira module, in the Connection field, select the Jira connection that uses the System Integration credentials, then click **OK** to save the module.


+++




### Scenario 6: WF-to-Jira Remove notes (Tasks and Issues)

+++**Expand to view instructions for configuring Scenario 6:WF-to-Jira Remove notes (Tasks and Issues)**

1. Click the **Templates** tab ![Templates icon](assets/templates-icon.png) in the left navigation panel.
1. Search for the template by using the search bar near the upper-left corner of the screen. You can search by template name or included applications.
1. Click the **Scenario 6: WF-to-Jira Remove notes (Tasks and Issues)** template.
 
   A view of the template opens, showing information and an animation of data flow.
1. In the first module, begin adding a webhook.
1. In the Connection field, select the Workfront connection that uses the System Integration credentials.
1. In the **Record Type** field, select `??`.
1. In the **State** field, select `New state`.
1. Configure the filter with the following operations, using the **And** option:

   |Field|Operator|Value|
   |---|---|---|
   |(Delete on Notes.)||| 
   |assignedToID|Equals|Enter the Workfront ID of the System Integration user|
   |projectID|Equals|Enter the ID of the project or projects that you want the webhook to watch.|
   |WF ID|Exists||

1. Enable the **Exclude updates made by this connection** option.
1. Click **Save** to save the webhook, then click **OK** to save the trigger module.
1. In the second module, set the following variables, then click **OK** to save the module.

   |Variable name|Variable value|
   |---|---|
   |defaultJiraReporterID|This is the ID of the default user when the Creator User doesn't exist in Jira. You can find this user ID by clicking on the profile of the user and checking the URL of the browser. Example: `https://myjira.atlassian.net/jira/people/<JiraUserID>`|
   |JiraBaseURL|The base URL of the Jira account you are connecting to.|
   |wfBaseURL|The base URL of the Workfront account you are connecting to.|

1. In **each** Workfront module, in the Connection field, select the Workfront connection that uses the System Integration credentials, then click **OK** to save the module.
1. In **each** Jira module, in the Connection field, select the Jira connection that uses the System Integration credentials, then click **OK** to save the module.


+++



### Scenario 7: WF-to-Jira New Attachments (Tasks and Issues)

+++**Expand to view instructions for configuring SScenario 7: WF-to-Jira New Attachments (Tasks and Issues)**

1. Click the **Templates** tab ![Templates icon](assets/templates-icon.png) in the left navigation panel.
1. Search for the template by using the search bar near the upper-left corner of the screen. You can search by template name or included applications.
1. Click the **Scenario 7: WF-to-Jira New Attachments (Tasks and Issues)** template.
 
   A view of the template opens, showing information and an animation of data flow.
1. In the first module, begin adding a webhook.
1. In the Connection field, select the Workfront connection that uses the System Integration credentials.
1. In the **Record Type** field, select `??`.
1. In the **State** field, select `New state`.
1. Configure the filter with the following operations, using the **And** option:

   |Field|Operator|Value|
   |---|---|---|
   |(Create on Document.)||| 
   |assignedToID|Equals|Enter the Workfront ID of the System Integration user|
   |projectID|Equals|Enter the ID of the project or projects that you want the webhook to watch.|

1. In the second module, set the following variables.

   |Variable name|Variable value|
   |---|---|
   |defaultJiraReporterID|This is the ID of the default user when the Creator User doesn't exist in Jira. You can find this user ID by clicking on the profile of the user and checking the URL of the browser. Example: `https://myjira.atlassian.net/jira/people/<JiraUserID>`|
   |JiraBaseURL|The base URL of the Jira account you are connecting to.|
   |wfBaseURL|The base URL of the Workfront account you are connecting to.|

1. Enable the **Exclude updates made by this connection** option.
1. Click **Save** to save the webhook, then click **OK** to save the trigger module.
1. In **each** Workfront module, in the Connection field, select the Workfront connection that uses the System Integration credentials, then click **OK** to save the module.
1. In **each** Jira module, in the Connection field, select the Jira connection that uses the System Integration credentials, then click **OK** to save the module.


+++



### Scenario 8: WF-to-Jira Remove Attachments (Tasks and Issues)

+++**Expand to view instructions for configuring Scenario 8: WF-to-Jira Remove Attachments (Tasks and Issues)**

1. Click the **Templates** tab ![Templates icon](assets/templates-icon.png) in the left navigation panel.
1. Search for the template by using the search bar near the upper-left corner of the screen. You can search by template name or included applications.
1. Click the **Scenario 8: WF-to-Jira Remove Attachments (Tasks and Issues)** template.
 
   A view of the template opens, showing information and an animation of data flow.
1. In the first module, begin adding a webhook.
1. In the Connection field, select the Workfront connection that uses the System Integration credentials.
1. In the **Record Type** field, select `??`.
1. In the **State** field, select `New state`.
1. Configure the filter with the following operations, using the **And** option:

   |Field|Operator|Value|
   |---|---|---|
   |(Delete on Document)||| 
   |assignedToID|Equals|Enter the Workfront ID of the System Integration user|
   |projectID|Equals|Enter the ID of the project or projects that you want the webhook to watch.|

1. In the second module, set the following variables.

   |Variable name|Variable value|
   |---|---|
   |defaultJiraReporterID|This is the ID of the default user when the Creator User doesn't exist in Jira. You can find this user ID by clicking on the profile of the user and checking the URL of the browser. Example: `https://myjira.atlassian.net/jira/people/<JiraUserID>`|
   |JiraBaseURL|The base URL of the Jira account you are connecting to.|
   |wfBaseURL|The base URL of the Workfront account you are connecting to.|

1. Enable the **Exclude updates made by this connection** option.
1. Click **Save** to save the webhook, then click **OK** to save the trigger module.
1. In **each** Workfront module, in the Connection field, select the Workfront connection that uses the System Integration credentials, then click **OK** to save the module.
1. In **each** Jira module, in the Connection field, select the Jira connection that uses the System Integration credentials, then click **OK** to save the module.


+++

