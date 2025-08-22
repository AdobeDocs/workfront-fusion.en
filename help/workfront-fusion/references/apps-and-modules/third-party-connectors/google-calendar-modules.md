---
title: Google Calendar modules
description: In an Adobe Workfront Fusion scenario, you can automate workflows that use Google Calendar, as well as connect it to multiple third-party applications and services.
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
---
# [!DNL Google Calendar] modules

In an Adobe Workfront Fusion scenario, you can automate workflows that use [!UICONTROL Google Calendar], as well as connect it to multiple third-party applications and services.

For instructions on creating a scenario, see the articles under [Create scenarios: article index](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

For information about modules, see the articles under [Modules: article index](/help/workfront-fusion/references/modules/modules-toc.md).

## Access requirements

You must have the following access to use the functionality in this article:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront plan*</td>
  <td> <p>[!UICONTROL Pro] or higher</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront license*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion license**</td> 
   <td>
   <p>Current license requirement: No Workfront Fusion license requirement.</p>
   <p>Or</p>
   <p>Legacy license requirement: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Current product requirement: If you have the [!UICONTROL Select] or [!UICONTROL Prime] Adobe Workfront Plan, your organization must purchase Adobe Workfront Fusion as well as Adobe Workfront to use functionality described in this article. Workfront Fusion is included in the [!UICONTROL Ultimate] Workfront plan.</p>
   <p>Or</p>
   <p>Legacy product requirement: Your organization must purchase Adobe Workfront Fusion as well as Adobe Workfront to use functionality described in this article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

To find out what plan, license type, or access you have, contact your Workfront administrator.

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Prerequisites

To use [!DNL Google Calendar] modules, you must have a [!DNL Google] account.

## Google Calendar API information

The Google Calendar connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td> https://www.googleapis.com/calendar/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API version</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v5.4.5</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Calendar] modules and their fields

When you configure [!DNL Google Calendar] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Google Calendar] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Triggers](#triggers)
* [Actions](#actions)
* [Iterators](#iterators)

### Triggers

* [Watch events](#watch-events)
* [Watch events (Instant)](#watch-events-instant)

#### Watch events

This trigger module executes a scenario when a new event is added, updated, deleted, started, or ended in the calendar you specify. The module returns all standard fields associated with the record or records, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Google Calendar] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Select the calendar you want the module to work with.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Choose whether you want to watch new events only, or new events and all changes.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>Enable this option to include events that were deleted.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>Enter text that you want to return results for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Set the maximum number of events that Workfront Fusion works with during one cycle (the number of repetitions per scenario run). If the value is set too high, the connection may be interrupted on the side of the given third-party service (timeout). Workfront Fusion has no influence on this. We recommend that you set a lower value and either define a higher value for the maximum number of cycles or run the scenario more frequently.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Watch events (Instant)

This trigger module uses a mailhook to create an email address that you can use as an invitee to events. The module starts a scenario based on events that the email address is invited to.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Mailhook] </td> 
   <td> <p>Select the mailhook that you want to use for this module. To create a new mailhooke, click <b>Add</b> and enter the connection you want to use for the mailhook.</p><p>For instructions about connecting your [!DNL Google Calendar] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Set the maximum number of events that Workfront Fusion works with during one cycle (the number of repetitions per scenario run). If the value is set too high, the connection may be interrupted on the side of the given third-party service (timeout). Workfront Fusion has no influence on this. We recommend that you set a lower value and either define a higher value for the maximum number of cycles or run the scenario more frequently.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [Create a calendar](#create-a-calendar)
* [Create an event](#create-an-event)
* [Delete an event](#delete-an-event)
* [Get events](#get-events)
* [Update an event](#update-an-event)

#### Create a calendar

This action module creates a calendar associated with the account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Google Calendar] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color] </td> 
   <td> <p>Select the color to associate with the calendar.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name] </td> 
   <td> <p>Enter or map a name for the new calendar.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an event] 

This action module creates an event.

You specify the calendar and the parameters for the event.

The module returns the ID of the  event and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>For instructions about connecting your [!DNL Google Calendar] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Select the calendar where you want the event to appear.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color]</td> 
   <td>Select the color that the event shows on the calendar.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Enter or map a name for the event. </p> <p>Note: If you have selected [!UICONTROL Quick add] in the [!UICONTROL Create an event] field, you can include the date and time of the event, and Workfront Fusion creates the event for that date and time. Example: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. If you selected [!UICONTROL Quick add] but do not include a date and time in the event name, the event is created from the current time and lasts an hour.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Enable this option if the event is an all-day event (does not require start and end times).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Enter or map the start date and time of the event. </p> <p>For a list of supported date formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Enter or map the end date and time of the event. </p> <p>For a list of supported date formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Enter or map a description for the event. This field supports HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Enter a location for the event in text form.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Enable this option to use default reminder settings. If you set a custom reminder in the [!UICONTROL Reminder] field, this value is set to No.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Add reminder for the event. For each reminder you want to add, click <b>Add item</b>, then select the method you want to be reminded with and define how long (in minutes) before the event you want to be reminded.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Add the attendees to the event. For each attendee, click <b>Add an attendee</b>, then enter or map their name and email address.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Select whether you want people who view your calendar to see you as Busy or Available during this event.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Select the visibility of this event. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>The event has the visibility that you have set in your calendar settings.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Anyone the calendar is shared with can see this event.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Only attendees can see this event.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Select whether to send notifications about the creation of a new event to all guests, to non-[!DNL Google Calendar] guests, or to no one.</p> <p>Tip: We recommend using the [!UICONTROL None] option only for migration use cases.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Enable this option if you want to guests to be able to modify this event.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Add any recurrence rules that you want to apply to this event. Each rule requires a list of [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE], and [!UICONTROL EXDATE] lines for a recurring event. Note that [!UICONTROL DTSTART] and [!UICONTROL DTEND] lines are not allowed in this field; event start and end times are specified in the start and end fields. This field is omitted for single events or instances of recurring events. For more information, see <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an event]

This action module deletes an event.

You specify the calendar and event ID.

The module returns the ID of the  event and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Google Calendar] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Select the calendar that contains the event you want to delete.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> Enter the event ID from a previously created [!DNL Google Calendar] event you want to delete.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get events] 

This module retrieves information about events in the selected calendar based on criterie you specify.

You specify the calendar and the parameters of the search.

The module returns the ID of the events and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>For instructions about connecting your [!DNL Google Calendar] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Select the calendar you want to retrieve events for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> Enter or map the date when the event starts. This module also retrieves events starting before this date, that are still occurring on the entered start date. </p> <p>For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Enter or map the date when the event ends. </p> <p> For a list of supported date and time formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Single events]</td> 
   <td> <p> Enable this option to treat recurring events as single instances. For example, if you have a weekly meeting and this option is enabled, the module returns each week's meeting as a separate event.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>Enter or map the search term that you want to search by. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td> <p>Select the order of the events returned in the result.</p> 
    <ul> 
     <li><strong>[!UICONTROL Start Time]</strong>: Order by the start date and time (ascending). This is only available when querying single events.</li> 
     <li><strong>[!UICONTROL Updated Time]</strong>: Order by last modification time (ascending).</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mazimum number of returned events]</td> 
   <td> <p>Set the maximum number of events Workfront Fusion returns during one execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an event] 

This action module changes an existing event.

You specify the calendar and event ID.

The module returns the ID of the  event and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Google Calendar] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Select the calendar you want to work with.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>Enter the event ID from the previously created [!DNL Google Calendar] event that you want to update.</p> </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Enter or map a name for the event. </p> <p>Note: If you have selected [!UICONTROL Quick add] in the [!UICONTROL Create an event] field, you can include the date and time of the event, and Workfront Fusion creates the event for that date and time. Example: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. If you selected [!UICONTROL Quick add] but do not include a date and time in the event name, the event is created from the current time and lasts an hour.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Enable this option if the event is an all-day event (does not require start and end times).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Enter or map the start date and time of the event. </p> <p>For a list of supported date formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Enter or map the end date and time of the event. </p> <p>For a list of supported date formats, see <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Enter or map a description for the event. This field supports HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Enter a location for the event in text form.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Enable this option to use default reminder settings. If you set a custom reminder in the [!UICONTROL Reminder] field, this value is set to No.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Add reminder for the event. For each reminder you want to add, click <b>Add item</b>, then select the method you want to be reminded with and define how long (in minutes) before the event you want to be reminded.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Add the attendees to the event. For each attendee, click <b>Add an attendee</b>, then enter or map their name and email address.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Select whether you want people who view your calendar to see you as Busy or Available during this event.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Select the visibility of this event. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>The event has the visibility that you have set in your calendar settings.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Anyone the calendar is shared with can see this event.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Only attendees can see this event.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Select whether to send notifications about the creation of a new event to all guests, to non-[!DNL Google Calendar] guests, or to no one.</p> <p>Tip: We recommend using the [!UICONTROL None] option only for migration use cases.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Enable this option if you want to guests to be able to modify this event.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Add any recurrence rules that you want to apply to this event. Each rule requires a list of [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE], and [!UICONTROL EXDATE] lines for a recurring event. Note that [!UICONTROL DTSTART] and [!UICONTROL DTEND] lines are not allowed in this field; event start and end times are specified in the start and end fields. This field is omitted for single events or instances of recurring events. For more information, see <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr> 

 </tbody> 
</table>

### Iterators

#### Iterate attachments

This action modules iterates through attachments to an event, and outputs each attachment in a separate bundle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> Select the module in this scenario that outputs the event that contains the attachments that you want to iterate. </td> 
  </tr> 
 </tbody> 
</table>

#### Iterate attendees

This action modules iterates through attendees for an event, and outputs each attendee in a separate bundle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> Select the module in this scenario that outputs the event that contains the attendees that you want to iterate. </td> 
  </tr> 
 </tbody> 
</table>





## Trigger a scenario before an event

You can trigger a scenario a specified time before an event with the help of standard [!DNL Google Calendar] email reminders and the [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] module.

1. Use the [!UICONTROL Google Calendar] >[!UICONTROL Update an event] module to add an email reminder to your event:

   ![Trigger scenario before event](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

1. Create a new scenario starting with the [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] module.

   1. Copy the mailhook's email address.
   1. Save the scenario and execute it.

1. In [!DNL Gmail], redirect the [!DNL Google Calendar] email reminders to the mailhook's email address:

   1. Open your **[!UICONTROL [!DNL Gmail] settings]**.
   1. Open the **[!UICONTROL Forwarding and POP/IMAP]** tab.
   1. Click **[!UICONTROL Add a forwarding address].**
   1. Paste the copied mailhooks's email address, click&#x200B;**[!UICONTROL Next]**, confirm by pressing **[!UICONTROL Proceed]** in the popup window, then click **[!UICONTROL OK]**.

   1. In Workfront Fusion, switch to the new scenario that should finish its execution by receiving the confirmation email.
   1. Click the bubble above the module to inspect the module's output.
   1. Expand the `Text` item and copy the Confirmation code:

      ![Confirmation code](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. In Gmail, paste the Confirmation code in the edit box and click&#x200B;**[!UICONTROL Verify]**:

      ![Paste code](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. Open the **[!UICONTROL Filters and Blocked Addresses]** tab.
   1. Click **[!UICONTROL Create a new filter]**.
   1. Setup a filter for all emails coming from `     calendar-notification@google.com` and click&#x200B;**[!UICONTROL Create a filter]**:
   1. Select **[!UICONTROL Forward it to]** and choose the mailhooks's email address from the list.
   1. Click **[!UICONTROL Create filter]** to create the filter.

1. (Optional) In Workfront Fusion, add the [!UICONTROL Text parser] > [!UICONTROL Match pattern] module after the [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] module to parse the email's HTML code to obtain any information you need.

   For example, you could configure the module as follows to obtain the event's ID:

   *Pattern*: `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *Text*: The `HTML content` item outputted from the [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] module.
