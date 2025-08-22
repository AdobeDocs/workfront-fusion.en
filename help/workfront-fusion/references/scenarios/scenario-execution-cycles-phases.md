---
title: Scenario Execution, Cycles, and Phases
description: This article describes events that occur while an Adobe Workfront Fusion scenario is running, such as initialization, operations, commits, and rollbacks.
author: Becky
feature: Workfront Fusion
exl-id: abf41be5-df32-4eaf-b3f4-93ddf005bfe3
---
# Scenario execution, cycles, and phases

Each scenario execution starts with the initialization phase, continues with at least one cycle composed of the operation and commit/rollback phases, and ends with the finalization phase

* Initialization
* Cycle #1
   * Operation (reading or writing)
   * Commit or rollback
* Cycle #2
   * Operation (reading or writing)
   * Commit or rollback
* ...
* Cycle #n
   * Operation (reading or writing)
   * Commit or rollback
* Finalization

On a smaller scale, each module also follows these phases. Information about the module phases can be found in the processed bundle information, found in the numbered bubble to the top right of each module after the scenario has run. For more information on locating processed bundle information, see [Information about processed bundles](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md#information-about-processed-bundles) in the article Scenario execution flow.

Information about the larger scenario phases can be found in the execution details. 

## Scenario execution phases

### Initialization

During the initialization phase, all necessary connections (connection to a database, email service, and so on) are created and checked to ensure that the module is capable of performing the intended operations.

### Cycles

Each cycle represents an indivisible unit of work composed of a series of operations, each with a commit or rollback. 

You can set the maximum number of cycles in the [!UICONTROL scenario settings] panel. The default number is 1.

* [Operation](#operation)
* [Commit](#commit)
* [Rollback](#rollback)

#### Operation

During the operation phase, a reading or writing operation is performed:

* A reading operation consists of obtaining data from a service that is then processed by other modules according to a predefined scenario. For example, the [!UICONTROL Workfront] >[!UICONTROL Watch records] module returns new bundles (records) created since the last scenario execution.
* A writing operation consists of sending data to a given service for further processing. For example, the Workfront >[!UICONTROL Upload Document] module uploads a file to Workfront.

#### Commit

If the operation phase is successful, the commit phase begins during which all operations performed by the modules are committed. This means that Workfront Fusion sends information to all the services involved in the operation phase about its success.

### Rollback

If an error occurs during the operation or commit phase on any module, the phase is aborted and the rollback phase is started, making all operations during the given cycle void. 

>[!IMPORTANT]
>
>All Workfront Fusion modules that support rollback (also known as transactionality) are marked with the ACID tag.
>
>![Acid modules](assets/acid-modules.png)
>
>Modules not marked with this tag cannot be reverted back to their initial state when errors occur in other modules. A typical example of a non-ACID module is the [!UICONTROL Email] >[!UICONTROL Send an Email] action. After the email is sent you cannot undo the sending.

### Finalization

During the finalization phase, open connections (for example, FTP connections, database connections, and so on) are closed and the scenario is completed.

## Resources

For more information, see [Configure scenario settings](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).
