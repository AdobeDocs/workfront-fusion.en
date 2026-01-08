---
title: View a specific scenario execution
description: You can view details of a specific scenario execution, including filtering and searching for scenario events.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
---
# View a specific scenario execution

You can view details of a specific scenario execution, including filtering and searching for scenario events.

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
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## View a specific execution

You can view an execution from the scenario's scenario history.


1. Click the **[!UICONTROL Scenario]** tab in the left panel, then click the scenario.

   Or

   If you are working on the scenario in the Scenario editor, click the left arrow ![Exit editing arrow](assets/exit-editing-arrow.png) near the upper-left corner of the window.

1. Click **History** near the name of the scenario.
    ![history tab](assets/history-tab.png)


1. Locate the execution you want to view, and click **Details** in the far right on the line for that execution. The [!UICONTROL details] link is visible only if the execution has details available.

   The scenario diagram opens, with the execution details panel open on the right.

   Modules that produced output for this execution are marked with green titles.

   Modules that did not run are dimmed.

1. To view output from a module, click the output details bubble near the module. The number in the bubble represents the number of bundles that the module output.

   ![Output bubble near a module](assets/output-bubble.png)

1. To view the bundles that passed through a filter, click the filter. The number near the filter represents the number of bundles that passed through the filter.
1. To search for a specific module or event in the execution panel, enter the search term into the **Search execution events** box. Results appear as you type.
1. To limit execution panel search results by status such as Success or Warning, click the **Status Filter** dropdown and select the status.




>[!NOTE]
>
>To create a link to a specific module, add `?moduleId=<module-id>` to the URL when viewing the following pages:
>
>* Scenario edit page (URL ends in `/edit`)
>* A specific scenarion execution (URL ends in `/logs/<log-id>`)
>
>`<module-id>` refers to the number next to the module label when viewing the scenario.
>
>This can be useful when debugging scenarios or copying module configuration.
