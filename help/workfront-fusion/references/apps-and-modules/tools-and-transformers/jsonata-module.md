---
title: JSONata modules
description: The Adobe Workfront Fusion JSONata connector provides a module to process data in JSON format so that Adobe Workfront Fusion can further work with the data content.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
---
# [!UICONTROL JSONata] modules

The [!DNL Adobe Workfront Fusion] [!UICONTROL JSONata] connector allows you to query JSON objects. This module does not require a connection.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] package</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] license</td> 
   <td> <p>New: [!UICONTROL Standard]</p><p>Or</p><p>Current: [!UICONTROL Work] or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] license**</td> 
   <td>
   <p>Current: No [!DNL Workfront Fusion] license requirement.</p>
   <p>Or</p>
   <p>Legacy: Any </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>[!UICONTROL Select] or [!UICONTROL Prime] [!DNL Workfront] plan: Your organization must purchase [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan: [!DNL Workfront Fusion] is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## JSONata modules and their fields

### Evaluate

This action module queries a JSON object and returns an array.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expression]</td> 
   <td>Enter the expression that you want to use to evaluate the JSON object. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data] </td> 
   <td> Enter the JSON object to evaluate.  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringify output] </td> 
   <td> Enable this option to convert output to a string.  </td> 
  </tr> 
  </tbody>
  </table>

>[!BEGINSHADEBOX]

**Example**:

The goal is to return an array of names from the following JSON object:

```JSON
{
  "people": [
    { "name": "Alice", "age": 30 },
    { "name": "Bob", "age": 25 },
    { "name": "Charlie", "age": 35 }
  ]
}
```

1. In the expression field, enter `people.name`.
1. In the data field, enter the JSON object.

The module returns an array of names pulled from the JSON object.

>[!ENDSHADEBOX]



### JSONata MCP

This action module generates JSONata expressions by analyzing provided input and output JSON structures.

The system knows what the data looks like before and after the transformation. It can generate JSONata expressions automatically at runtime based on the scenario, allowing you to customize or fine-tune those expressions without deep technical knowledge.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Select the connection that you use to connect to the large language model (LLM) that you want to use for this module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input schema]</td> 
   <td> <p>Enter or map the input schema to use for this JSON expression.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output schema]</td> 
   <td> <p>Enter or map the output schema to use for this JSON expression.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

What is JSONata, and what are input/output schemas?
JSONata is a tool used to transform and query JSON data (which is the standard format for structured information in APIs, apps, etc.).
What problem does JSONata solve?
Previously, users had to manually write JSONata expressions to transform their data. For example, if you wanted to extract just the email subjects or reformat data before sending it to Slack, you had to write the exact logic yourself.
Now, the MCP server provides both the input and output schemas (in JSON format). This means:
The system knows what the data looks like before and after the transformation.
It can generate JSONata expressions automatically at runtime based on the scenario.
Users can easily customize or fine-tune those expressions without deep technical knowledge.
Why is this useful?
With this feature, customers can now design automation scenarios more easily. They can manipulate the data flowing between services without writing complex code. JSONata becomes a powerful but simple way to:
Format messages
Filter data
Merge fields
Customize outputs for downstream tools
In short, JSONata makes it easy for users to shape their data exactly how they need it, right inside the MCP-powered workflow.
If you have any questions or would like to schedule a call to go over things in more detail, feel free to reach out—happy to talk anytime. Thanks so much for taking the time to review this!

-->
