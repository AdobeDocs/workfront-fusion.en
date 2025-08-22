---
title: Microsoft Office 365 Calendar
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Microsoft Office 365 Calendar, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: fdecf740-e735-4569-b1a2-7c25c751ba42
---
# [!DNL Microsoft Office 365 Calendar] 

In an Adobe Workfront Fusion scenario, you can automate workflows that use [!DNL Microsoft Office 365 Calendar], as well as connect it to multiple third-party applications and services.

## Access requirements

+++ Expand to view access requirements for the functionality in this article.

You must have the following access to use the functionality in this article:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront package</td> 
   <td> <p>Any</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license</td> 
   <td> <p>New: Standard</p><p>Or</p><p>Current:  Work or higher</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>Current: No Workfront Fusion license requirement</p>
   <p>Or</p>
   <p>Legacy: Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>New:</p> <ul><li>Select or Prime Workfront package: Your organization must purchase Adobe Workfront Fusion.</li><li>Ultimate Workfront package: Workfront Fusion is included.</li></ul>
   <p>Or</p>
   <p>Current: Your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

To use [!DNL Microsoft Office 365 Calendar] modules, you must have a [!DNL Microsoft Office 365 Calendar] account.

## Microsoft Office 365 Calendar API information

The Microsoft Office 365 Calendar connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API version</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## Connecting the [!DNL Office 365 Calendar] service to Workfront Fusion

For instructions about connecting your [!DNL Office 365 Calendar] account to [!UICONTROL Workfront Fusion], see [Create a connection to [!UICONTROL Adobe Workfront Fusion] - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Some Microsoft apps use the same connection, which is tied to individual user permissions. Therefore, when creating a connection, the permissions consent screen displays any permissions that were previously granted to this user's connection, in addition to any new permissions needed for the current application. 
>
>For example, if a user has "Read table" permissions granted via the Excel connector and then creates a connection in the Outlook connector to read emails, the permissions consent screen will show both the already granted "Read table" permission and the newly required "Write email" permission.

## [!DNL Microsoft Office 365 Calendar] modules and their fields

When you configure [!DNL Microsoft Office 365 Calendar] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Microsoft Office 365 Calendar] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Event](#event)
* [Calendar](#calendar)
* [Other](#other)

### Event 

* [[!UICONTROL Create an Event]](#create-an-event)
* [[!UICONTROL Delete an Event]](#delete-an-event)
* [[!UICONTROL Get an Event]](#get-an-event)
* [[!UICONTROL Search Events]](#search-events)
* [[!UICONTROL Update an Event]](#update-an-event)
* [[!UICONTROL Watch Events]](#watch-events)

#### [!UICONTROL Create an Event]

This action module creates a new event.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Enter or map a title for the created event.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start date]</td> 
   <td> Enter a single point of time when the event starts in a combined date and time representation. Use the format <code>{date}T{time}</code>; for example, <code>2017-08-29T04:00:00.0000000</code>. For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End date]</td> 
   <td> Enter a single point of time when the event ends in a combined date and time representation. Use the format <code>{date}T{time}</code>; for example, <code>2017-08-29T04:00:00.0000000</code>. For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder on]</td> 
   <td>Select whether you want to activate a reminder for this event.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder]</td> 
   <td>Enter or map he number of minutes before the start of the event when the reminder should trigger.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Select the importance of this event.</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>Select the sensitivity of this event.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>The recipient sees a "[!UICONTROL Please treat this as Personal]" message.</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>The recipient sees a "[!UICONTROL Please treat this as Private]" message. This event isn't forwarded or redirected by the recipient's inbox rules.</p> </li> 
     <li> <p><strong>[!UICONTROL Confidential]</strong> </p> <p>The recipient sees a "[!UICONTROL Please treat this as Confidential]" message. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content type]</td> 
   <td>Select whether the body content is plain text or HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td>Enter or map the body of the message associated with the event. It can be in HTML or text format (as specified in the [!UICONTROL Body Content Type] field above).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Location]</td> 
   <td> <p>Enter or map the event location details.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Response requested]</td> 
   <td>Select <strong>[!UICONTROL Yes]</strong> to request the invitee to send a response to the event invitation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show as]</td> 
   <td> <p>Select how you want the event to appear to people who view your calendar.</p> 
    <ul> 
     <li>[!UICONTROL Free]</li> 
     <li>[!UICONTROL Tentative]</li> 
     <li>[!UICONTROL Busy]</li> 
     <li>[!UICONTROL Out of office]</li> 
     <li>[!UICONTROL Working elsewhere]</li> 
     <li>[!UICONTROL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attendees]</p> </td> 
   <td> <p>For each attendee that you want to invide, click <b>Add item</b> and enter the following:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter or map the attendee's name.</p> </li> 
     <li> <p><strong>[!UICONTROL Email]</strong> </p> <p>Enter or map the attendee's email address.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Categories]</td> 
   <td>For each category that you want the event to display as on the calendar, click <b>Add item</b> and enter or map the category.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Event]

This action module deletes an existing event.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Enter or map the ID of the event you want to delete.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Event]

This action module retrieves details of the specified event.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Enter or map the ID of the event you want to retrieve details about.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Events]

This search module retreves details of an event when the event is created, updated, deleted, started, or ended in the selected calendar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Select the [!UICONTROL calendar group] that contains the calendar where you want to watch events.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>Select the specific calendar that you want to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Set the filter conditions to filter results. You can filter by the following properties:</p> 
    <ul> 
     <li>[!UICONTROL Subject]</li> 
     <li>[!UICONTROL Event ID]</li> 
     <li>[!UICONTROL Created Date Time]</li> 
     <li>[!UICONTROL Last Modified Date Time]</li> 
     <li>[!UICONTROL Body Preview]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td> <p>Select how you want to order the results.</p> 
    <ul> 
     <li><strong>[!UICONTROL Subject]</strong>, ascending or descending</li> 
     <li><strong>[!UICONTROL Created Date Time]</strong>, ascending or descending</li> 
     <li><strong>[!UICONTROL Last Modified Date Time]</strong>, ascending or descending</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Enter the maximum number of events Workfront Fusion should return during one scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an Event]

This action module updates an existing event.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td>Enter, map, or select the ID of the event you want to update.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Enter or map a new title for the event.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start date]</td> 
   <td> Enter a single point of time when the event starts in a combined date and time representation. Use the format <code>{date}T{time}</code>; for example, <code>2017-08-29T04:00:00.0000000</code>. For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End date]</td> 
   <td> Enter a single point of time when the event ends in a combined date and time representation. Use the format <code>({date}T{time}</code>; for example, <code>2017-08-29T04:00:00.0000000</code>. For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder on]</td> 
   <td>Select whether you want to activate a reminder for this event.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder]</td> 
   <td>Enter or map he number of minutes before the start of the event when the reminder should trigger.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Select the importance of this event.</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>Select the sensitivity of this event.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>The recipient sees a "[!UICONTROL Please treat this as Personal]" message.</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>The recipient sees a "[!UICONTROL Please treat this as Private]" message. This event isn't forwarded or redirected by the recipient's inbox rules.</p> </li> 
     <li> <p><strong>[!UICONTROL Confidential]</strong> </p> <p>The recipient sees a "[!UICONTROL Please treat this as Confidential]" message. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content type]</td> 
   <td>Select whether the body content of the message associated with the event is plain text or HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td>Enter or map the body of the message associated with the event. It can be in HTML or text format (as specified in the [!UICONTROL Body Content Type] field above).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Location]</td> 
   <td> <p>Enter the event location details.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Response requested]</td> 
   <td>Select <strong>[!UICONTROL Yes]</strong> to request the invitee to send a response to the event invitation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show as]</td> 
   <td> <p>Select how you want the event to appear to people who view your calendar.</p> 
    <ul> 
     <li>[!UICONTROL Free]</li> 
     <li>[!UICONTROL Tentative]</li> 
     <li>[!UICONTROL Busy]</li> 
     <li>[!UICONTROL Out of office]</li> 
     <li>[!UICONTROL Working elsewhere]</li> 
     <li>[!DNL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attendees]</p> </td> 
   <td> <p>Add attendees of the event.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Enter the attendee's name.</p> </li> 
     <li> <p><strong>[!UICONTROL Email]</strong> </p> <p>Enter the attendee's email address.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>Enter or map the categories that you want the event to display as on the calendar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Events]

This trigger module retrieves details of an event when the event is created, updated, deleted, started, or ended in the selected calendar.

>[!NOTE]
>
>To watch for deleted occurrences of an event series, select [!UICONTROL By Updated Time] in the [!UICONTROL Watch events] field. This module does not watch for deleted single events or deleted event series.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch events]</td> 
   <td> <p>Select how you want to watch events.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL By Created Time]</strong> </p> <p>Watch for new events.</p> </li> 
     <li> <p><strong>[!UICONTROL By Updated Time]</strong> </p> <p>Watch for updated events.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Select the [!UICONTROL calendar group] that contains the calendar where you want to watch events.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>Select the specific calendar that you want to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Set the filter conditions to filter results by subject, event ID, or body.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter the maximum number of messages Workfront Fusion should return during one scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Calendar

* [[!UICONTROL Create a Calendar]](#create-a-calendar)
* [[!UICONTROL Delete a Calendar]](#delete-a-calendar)
* [[!UICONTROL Get a Calendar]](#get-a-calendar)
* [[!UICONTROL List Calendars]](#list-calendars)
* [[!UICONTROL Update a Calendar]](#update-a-calendar)



#### [!UICONTROL Create a Calendar]

This action module creates a new calendar in your Office 365 account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar name]</td> 
   <td> <p>Enter a name for the new calendar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Calendar]

This action module deletes an existing calendar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td>Enter the [!UICONTROL Calendar] ID for the calendar you want to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Calendar]

This action module retrieves details about a single calendar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Enter or map the ID of the calendar you want to retrieve details about.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Calendars]

This search module retrieves a list of all of the authenticated user's calendars.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Select the [!UICONTROL calendar group] that contains the calendars you want to list.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Enter the maximum number of calendars Workfront Fusion should return during one scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Calendar]

This action module edits an existing calendar.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td>Enter the [!UICONTROL Calendar ID] for the calendar you want to update. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Calendar name]</td> 
   <td> <p>Enter a new name for the calendar.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Other

#### [!UICONTROL Make an API Call]

This module allows you to perform a custom API call.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Office 365] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Enter a path relative to <code>https://graph.microsoft.com</code>. Example:<code> /v1.0/me/events</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object. For example, <code>{"Content-type":"application/json"}</code>. Workfront Fusion adds the authorization headers for you.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Add the query for the API call in the form of a standard JSON object.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:   <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
