---
title: Adobe Workfront Content and Approvals modules
description: With the Adobe Workfront Content and Approvals modules, you can get approval details, make a decision on an asset, add or delete approval participants, add or update approval stages, lock or unlock stages, and make custom API calls.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# Adobe Workfront Unified Review and Approvals modules

With the Adobe Workfront Unified Review and Approvals modules, you can get approval details, make a decision on an asset, add or delete approval participants, add or update approval stages, lock or unlock stages, and make custom API calls.

For information about Workfront unified review and approvals, see [Unified review and approval overview](https://experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/document-approvals-overview) in the Workfront documentation.

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

## Prerequisites

You must have the following to access Workfront Content and Approvals:

* You must be on a version of Workfront that supports Adobe cloud storage. If your organization is not already on a supported version, contact your Adobe account representative.

## Connect to Adobe Workfront Unified Review and Approvals

### Adobe Workfront Approvals connection

### Adobe Workfront server-to-server connection

## Adobe Workfront Unified Review and Approvals modules

When you configure Workfront modules, Workfront Fusion displays the fields listed below. Along with these, additional Workfront fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Searches]()
* [Actions]()
* [Other]()

### Searches



#### Get approval details

This search module retrieves approval details for an asset.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Document</p>
      </td>
      <td>Enter or map the ID of the asset that you want to retrieve approval details for.</td> 
      </tr>
  </tbody>
</table>



### Actions

* [Add or update participants](#add-or-update-participants)
* [Create or update an approval stage](#create-or-update-an-approval-stage)
* [Delete participants](#delete-participants)
* [Lock a stage]()
* [Make a decision]()
* [Unlock a stage]()


#### Add or update participants

This action module adds or updates participants on the default stage on an approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Document ID</p>
      </td>
      <td>Enter or map the ID of the asset that you want to add or update a participant for.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Add participants to stages</p>
      </td>
      <td>For each stage that you want to add participants to, click <b>Add item</b> and enter the stage.<p> Then, for each participant that you want to add to the stage, click <b>Add item</b> and enter the participant details.</p>
      <ul>
      <li><b>Participant ID</b><p>Enter or map the ID of the participant.</p></li>
      <li><b>Participant type</b><p>Select whether the participant is a user or a tea.</p></li>
      <li><b>Participant role</b><p>Select whether the participant is an approver or a reviewer.</p></li>
      </ul> 
      </td> 
      </tr>
  </tbody>
</table>

#### Create or update an approval stage

This action module creates or updates an approval stage with the given stage data.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to create or update a stage for.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Stages</p>
      </td>
      <td>For each stage that you want to add participants to, click <b>Add item</b> and enter the stage data.<p>For specifics, see <a href="#stages-fields" class="MCXref xref" >Stages fields</a> in this article. </p> </td> 
      </tr>
  </tbody>
</table>

##### Stages fields

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Stage name</td>
      <td>Enter or map a name for the stage.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Deadline date</p></td>
      <td>If the deadline is a specific date, enter or map the date.</td> 
      </tr>
  </tbody>
     <tr>
      <td role="rowheader"><p>Deadline business days</p></td>
      <td>If the deadline is after a specific number of business days, enter or map the number of days.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Deadline time</p></td>
      <td>If the deadline is a specific time, enter or map the time.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Participants</p></td>
      <td>For each participant that you want to add to the stage, click <b>Add item</b> and enter the participant details.      
      <ul>
      <li><b>Participant ID</b><p>Enter or map the ID of the participant.</p></li>
      <li><b>Participant type</b><p>Select whether the participant is a user or a team.</p></li>
      <li><b>Participant role</b><p>Select whether the participant is an approver or a reviewer.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Auto lock enabled</p></td>
      <td>Specify whether you want to auto-lock the stage.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Parent IDs</p></td>
      <td>For each parent that you want to add to the stage, click <b>Add item</b> and enter the Parent ID.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Triggers</p></td>
      <td>To configure a trigger for this approval stage, click <b>Add item</b> and enter the trigger details.      <ul>
      <li><b>Type</b><p>Select <b>Activation</b></p></li>
      <li><b>When</b><p>Select whether to trigger the stage when the approval is created or when another stage is complete.</p></li>
      <li><b>Stages</b><p>For each stage that you want to add to the trigger, click <b>Add item</b> and enter or map the stage ID.</p></li>
      <li><b>Decisions</b><p>For each decision that you want to add to the trigger, click <b>Add item</b> and enter or map the decision.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Custom message</p></td>
      <td>Enter or map a custom message for the stage.</td> 
      </tr>
</table>

#### Delete participants

This action module deletes participants from an approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to delete participants from.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant type</p>
      </td>
      <td>Select whether the participants is a user or a team.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant ID</p>
      </td>
      <td>Enter or map the ID of the participant.</td> 
      </tr>
  </tbody>
</table>

#### Lock a stage

This action modules locks the specified approval stage and sets the stage to inactive.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to lock.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Stage ID</p>
      </td>
      <td>Enter or map the ID of the stage that you want to lock.</td> 
      </tr>
  </tbody>
</table>

#### Make a decision

This action module applies a decision to an approval or approval stage.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to lock.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Decision</p></td>
      <td>Select the decision to apply to the approval or stage.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Stage IDs</p>
      </td>
      <td>For each stage that you want to apply the decision to, click <b>Add item</b> and enter the stage ID.</td> 
      </tr>
  </tbody>
</table>

#### Unlock a stage

This action modules unlocks the specified approval stage and sets the stage to active.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to unlock.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Stage ID</p>
      </td>
      <td>Enter or map the ID of the stage that you want to lock.</td> 
      </tr>
  </tbody>
</table>

### Other

#### Bulk lookup approvals

This module retrieves details of approvals for a list of documents of a specific type.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document IDs</p></td>
      <td>For each document that you want to retrieve approval details for, click <b>Add item</b> and enter the document ID.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Maximum number of returned results
         </td>
         <td>
              Enter or map the maximum number of results you want the module to return during each scenario execution cycle. 
         </td>
       </tr>
  </tbody>
</table>

#### Make a custom API call

This module makes a custom API call to the Adobe Workfront Unified Review and Approvals API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Relative path</p>
      </td>
      <td>
        <p>Enter a path relative to <code>https://workfront.adobe.io</code>. For example, <code>/unified-approvals/public/api/v1/approvals/&lt;ASSET_TYPE&gt;/&lt;ASSET_ID&gt;</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Method</p>
      </td>
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP request methods</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">Headers</td>
      <td>
        <p>Add the headers of the request in the form of a standard JSON object.</p>
        <p>For example, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion adds authorization headers automatically.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>For each key/value pair that you want to add to the query string, click <b>Add item</b> and enter the key and value.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### Uncategorized

#### Bulk delete templates

This module deletes the specified approval templates.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Template IDs</p></td>
      <td>For each template that you want to delete, click <b>Add item</b> and enter the template ID.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Maximum number of deleted templates
         </td>
         <td>
              Enter or map the maximum number of templates you want the module to delete during each scenario execution cycle. 
         </td>
       </tr>
  </tbody>
</table>

#### Create an approval

This action module creates an approval for a document on Adobe cloud storage, including stage data or a template.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to create an approval for.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Stages</p>
      </td>
      <td>For each stage that you want to add, click <b>Add item</b> and enter the stage data.<p>For specifics, see <a href="#stages-fields" class="MCXref xref" >Stages fields</a> in this article. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Template ID</p></td>
      <td>Enter or map the ID of the template that you want to use for this approval.</td> 
      </tr>
  </tbody>
</table>

#### Create a template

#### Delete Approval

#### Delete a Stage

#### Delete Decision on Stage

#### Delete Decisions

#### Delete Template

#### Get Suggested Approvals

#### Get Suggested Participants

#### Get Template

#### Make Decision on Stage

#### Remind Participant

#### Remind Participant on Stage

#### Remind Undecided Participants

#### Remind Undecided Participants on a Stage

#### Search AI brand reviews

#### Update all stages

#### Update a stage

#### Update Template

#### List Bots

#### List Templates


