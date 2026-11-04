---
title: Adobe CX Enterprise Coworker modules
description: Use the Adobe CX Enterprise Coworker connector in Adobe Workfront Fusion to send a natural-language prompt to Coworker and use its response in a scenario.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
---
# Adobe CX Enterprise Coworker modules

Use the Adobe CX Enterprise Coworker connector in Adobe Workfront Fusion to send a natural-language prompt to Coworker and use its response in a scenario. Coworker interprets your request and can use tools available to your account to carry out the work.

The connector provides two modules:

* **[!UICONTROL Run a Prompt]** starts a new request and, by default, waits for the result.
* **[!UICONTROL Get Execution Status]** checks a request that you started earlier.

## Access requirements

<!-- BECKY CHECK ME: This table is copied from other Fusion connector articles. The source material does not list access requirements, but says you need an Adobe account that has access to Coworker. Confirm the requirements and whether Coworker needs its own license or entitlement. -->

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
   <p>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prerequisites

YOu must have an Adobe account that has access to Adobe CX Enterprise Coworker.

## Connect Adobe CX Enterprise Coworker to Workfront Fusion

Sign in with an Adobe account that has access to Coworker and any services needed for your request.

To create a connection:

1. In the Adobe Fusion MCP module, click **[!UICONTROL Add]** next to the **Connection** field.
1. Fill in the following fields:

   <table style="table-layout:auto">
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">Connection name</td>
        <td>
          <p>Enter a name for this connection.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Environment</td>
        <td>
          <p>Select whether you are connecting to a production or non-production environment.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Type</td>
        <td>
          <p>Select whether you are connecting to a service account or a personal account.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Client ID</td>
        <td>
          <p>Enter or map an optional override for this connection. Otherwise, use this account type's platform-managed clientId. Register the displayed Fusion callback URL for the dedicated Coworker account..</p>
        </td>
      <tr>
        <td role="rowheader">Client secret</td>
        <td>
          <p>Enter or map an optional override for this connection. Otherwise use this account type's platform-managed clientSecret. Use credentials issued for the configured IMS environment.</p>
        </td>
    </tbody>
   </table>

1. Click **[!UICONTROL Continue]**.

If you cannot sign in or use a required service, contact your administrator.

## Adobe CX Enterprise Coworker modules and their fields

>[!WARNING]
>
>Never include passwords or other credentials in a prompt.

### Get Execution Status

This action module checks the current state of a task started by **[!UICONTROL Run a Prompt]**.

This module checks the task once. It does not start a new task or keep checking until the task completes. If the result is still pending, check again later.

>[!NOTE]
>
>Do not convert the Task ID to a number, round it, or reformat it. If Coworker answered the original prompt immediately without a Task ID, you do not need to check the status.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Include raw result] <i>(Optional, advanced)</i></td> 
   <td> <p>This option is off by default. Include the full Coworker response in the output. The response might contain sensitive information.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Select the same connection that you used in the original <b>[!UICONTROL Run a Prompt]</b> execution.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Task ID]</td> 
   <td> <p>Map the Task ID returned by <b>[!UICONTROL Run a Prompt]</b>. Keep it as text exactly as returned.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Run a Prompt

This action module sends an instruction to Coworker, such as summarizing text or gathering information using tools available to your account.

Each run sends the prompt once and starts a new conversation. You do not need to select an AI model or provide a separate AI-provider key.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Select your Coworker connection. For instructions, see <a href="#connect-adobe-cx-coworker-to-workfront-fusion" class="MCXref xref">Connect Adobe CX Enterprise Coworker to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL User prompt]</td> 
   <td> <p>Enter your instruction. You can use multiple lines and map information from earlier modules.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Wait for completion] <i>(Optional, advanced)</i></td> 
   <td> <p>This option is on by default. Enable this option if you want the module to wait for the task to finish or require attention. Turn it off to return the initial result immediately.</p><p>For more information, see <a href="#wait-for-completion">Wait for completion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Include raw result] <i>(Optional, advanced)</i></td> 
   <td> <p>This option is off by default. Enable this option if you want the module to include the full Coworker response in the output. The response might contain sensitive information.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
> We recommend leaving **[!UICONTROL Include raw result]** off unless you need the full response for a specific purpose. Raw results might contain sensitive information, and they are not a guaranteed complete record of every action. Review what a raw result contains before you save it, share it, or pass it to another service.

#### Wait for completion

When **[!UICONTROL Wait for completion]** is on, the module checks the task after a five-second wait. If the task is still pending, the module waits another five seconds before checking again. Each check also takes time to receive a response. Checking the status does not send the prompt again.

Waiting stops when the task completes, fails, is canceled or rejected, or needs your input or authorization. If Coworker provides an immediate answer, the module returns it without further checks.

When **[!UICONTROL Wait for completion]** is off, the module returns the first result without waiting for the task to finish. Inspect **[!UICONTROL State]**, **[!UICONTROL Completed]**, and **[!UICONTROL Requires attention]** to decide what to do next. A task can already be completed when the first result arrives.

Waiting is subject to Fusion's module timeout. If the module times out or stops, Coworker might continue working. In that case, you might not receive an output or a task ID.

For longer work, turn waiting off and save the initial **[!UICONTROL Task ID]** so you can check the task later. Do not automatically run the prompt again after a timeout. The first request might already be in progress, and repeating it can duplicate changes.


## Module output

Both modules return the following information when they finish without an error.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p>Identifies the task. This is empty when Coworker provides an immediate answer without creating a task. Use this value with <b>[!UICONTROL Get Execution Status]</b>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Context ID]</td> 
   <td> <p>Identifies the conversation. It is not an input for continuing the conversation.</p><p>For more information, see <a href="#use-previous-answers">Use previous answers</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td> <p>The current task state. See <a href="#task-states" class="MCXref xref">Task states</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Completed]</td> 
   <td> <p>True when the task completes or Coworker provides an immediate answer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Requires attention]</td> 
   <td> <p>True when Coworker needs input or authorization.</p><p>For more information, see <a href="#requests-that-need-attention">Requests that need attention</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Final assistant text]</td> 
   <td> <p>The final answer when the task is completed. This is empty while the task is pending or requires attention. A completed response can also have no answer text.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text artifacts (may include intermediate text)]</td> 
   <td> <p>Text returned during the work. Each item can include an Artifact ID, Name, and Text. These items are not necessarily final answers.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Raw result (opt-in)]</td> 
   <td> <p>The full response. This is included only when <b>[!UICONTROL Include raw result]</b> is on.</p> </td> 
  </tr> 
 </tbody> 
</table>

Use **[!UICONTROL Final assistant text]** for the answer instead of combining all text artifacts. Artifacts can include progress descriptions or other intermediate text.

### Requests that need attention

Coworker might need more information or authorization before it can continue. When this happens, **[!UICONTROL Requires attention]** is true and **[!UICONTROL Completed]** is false. Route the result to a person instead of treating it as completed work.

These modules cannot answer a follow-up question or approve an action on your behalf. **[!UICONTROL Get Execution Status]** can check whether the task's state has changed, but it does not resolve the request for input or authorization.

### Use previous answers

Every **[!UICONTROL Run a Prompt]** execution starts a new conversation. To refer to an earlier answer, include the relevant question and answer as text in your new prompt. This gives Coworker context, but it does not resume the previous conversation.

**[!UICONTROL Context ID]** identifies the conversation associated with the result. You cannot supply it to these modules to continue a conversation.

>[!IMPORTANT]
>
>**[!UICONTROL Completed]** does not guarantee that the requested business action succeeded. For example, Coworker might finish by explaining that a required tool was unavailable. Review the answer and verify any required result before you take the next action.

### Task states

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"><code>submitted</code>, <code>working</code></td> 
   <td> <p>The task is pending. <b>[!UICONTROL Completed]</b> is false. <b>[!UICONTROL Run a Prompt]</b> continues waiting when waiting is on. Otherwise, save the Task ID and check later.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>completed</code></td> 
   <td> <p><b>[!UICONTROL Completed]</b> is true. Review <b>[!UICONTROL Final assistant text]</b> and the expected result.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>input-required</code>, <code>auth-required</code></td> 
   <td> <p>The task needs attention. <b>[!UICONTROL Completed]</b> is false and <b>[!UICONTROL Requires attention]</b> is true. Waiting stops. Route the result for human review.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>failed</code>, <code>canceled</code>, <code>rejected</code></td> 
   <td> <p>The module reports an error instead of a normal result.</p> </td> 
  </tr> 
 </tbody> 
</table>

A pending result, or a result that requires attention, is not a successful completion, even if the module returns without an error.

## Examples

### Summarize an update

1. Add **[!UICONTROL Run a Prompt]** and select your connection.
1. Enter the following in the **[!UICONTROL User prompt]** field:

   ```text
   Summarize the following project update in three bullet points.
   Use only the supplied text; do not call tools or change any records.

   The planning workshop is complete. Two dependencies need confirmation.
   The team will review the delivery estimate on Friday.
   ```

1. Leave **[!UICONTROL Wait for completion]** on and **[!UICONTROL Include raw result]** off.
1. If **[!UICONTROL Requires attention]** is true, route the result for human review. If **[!UICONTROL Completed]** is true, map **[!UICONTROL Final assistant text]** into your next step.

AI-generated wording can vary. Review results where accuracy matters.

### Check a longer task later

1. Add **[!UICONTROL Run a Prompt]**, select your connection, and enter your instruction.
1. Turn **[!UICONTROL Wait for completion]** off.
1. Inspect the initial result.

   * If the task is completed, process the result.
   * If the task requires attention, route the result for review.
   * If the task is pending, save the **[!UICONTROL Task ID]** as text and note which connection you used.

1. Later, use **[!UICONTROL Get Execution Status]** with that connection and Task ID.
1. If the task is still pending, arrange another check within your scenario's limits. Process the result once on completion, and handle attention or errors separately.

Do not run the original prompt again just to check its progress.

## Usage considerations

* Coworker can use tools and perform actions allowed by your account, including changes to records. Use trusted prompts and an account with appropriate access.
* These modules do not provide a way to restrict individual tools. Instructions such as "do not change anything" describe your intent, but they are not an enforced read-only mode.
* Available tools and skills vary by account. The connector does not provide a skill selector or guarantee a particular action, such as creating a journey or updating a project. Do not assume that requests that need approval will complete unattended.
* The connector starts and checks Coworker requests. It does not monitor project changes or automatically save answers to another application. Add the appropriate trigger, storage, and follow-on modules to your scenario as needed.
* AI-generated answers can be incomplete or inaccurate. Validate important results before you use them to make changes or decisions.
* The connector does not automatically retry a failed request. Make sure your scenario's error handling does not repeat a prompt whose outcome is uncertain.

## Troubleshooting

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">A required field is missing</td> 
   <td> <p>Select a connection and enter the required prompt or Task ID.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sign-in fails or access is denied</td> 
   <td> <p>Sign in again, and check that your Adobe account has access to Coworker and the required services. Contact your administrator if needed.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Task not found</td> 
   <td> <p>Check that the Task ID is unchanged and that you are using the original connection. A new task might not be visible immediately. Check the status later instead of sending the prompt again.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">A status check fails</td> 
   <td> <p>If the error includes the accepted Task ID, use <b>[!UICONTROL Get Execution Status]</b> to investigate that task. Do not restart the prompt automatically.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Run a Prompt times out or loses its response</td> 
   <td> <p>The task might have started even if you did not receive its ID. Investigate before you repeat the request, to avoid duplicate work.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Fusion times out while waiting</td> 
   <td> <p>Coworker might still be working. Check the task if you have its ID. For future long tasks, turn waiting off and save the initial ID first.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Coworker or a required service is unavailable</td> 
   <td> <p>Share the displayed error with your administrator, without credentials or sensitive result content.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- BECKY CHECK ME: Confirm the exact module and field labels in the UI (Run a Prompt, Get Execution Status, User prompt, Wait for completion, Include raw result, Task ID, and the output item names). Also confirm that the module is listed under "Adobe CX Enterprise Coworker" in the app picker. -->
