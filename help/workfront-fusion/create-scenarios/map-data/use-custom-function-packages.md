---
title: Use Custom Function Packages
description: When you map items, you can use functions to create simple or complex formulas.
author: Becky
feature: Workfront Fusion
---

# Use custom function packages

Packages let you build and run your own custom logic inside Adobe Workfront Fusion, without leaving the Fusion interface. When the standard modules don't do exactly what you need, you can use a function to transform data, do a calculation, call an external service, or wrap a routine you want to reuse. You can then test it, make it live, and use it from your scenarios.

Complex functions may require resources such as variables and dependencies such as libraries. For these functions, you can create a package that includes the function and its resources.

A package can include:

* **Functions**: The logic that runs during a scenario execution.
* **Variables**: Reusable values, such as a base URL or an API key, that the function in the package uses.
* **Dependencies**: Outside libraries your functions may rely on.
* **History**: Earlier versions of each function, saved automatically, that you can reference.


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
   <p><ul><li>If your organization has a Select or Prime Workfront package that does not include Workfront Automation and Integration, your organization must purchase Adobe Workfront Fusion.</li><li>You must have an Adobe App Builder license to use custom functions.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

For more detail about the information in this table, see [Access requirements in documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Set up the runtime environment connection

>[!NOTE]
>
>This is a one-time setup.

The first time your team uses this feature, you must set up the environment that runs the functions. You only do this once per team.

1. Click the **Packages** ![Packages icon](assets/packages-icon.png) tab in the left navigation panel.

   If the environment has not been set up, the **Runtime Environment Not Configured** screen appears.

1. Click **Initialize runtime**.

1. To enter a name other than the default name, type the name in the **Connection name** field.

1. Select the Adobe App Builder project that this package will belong to::

   * To select an existing project, begin typing the project name, then select it when it appears.
   * To create a new project, enter a name that doesn't already exist and click **Create new**.
   * If you leave this empty, Fusion uses a default project.

1. Select **Continue**.

   Fusion finishes the setup and you're ready to create packages.

   Your environment appears as a connection tab at the top of the page. 
   
   ![Environment as connection tab](assets/package-environment-as-connection.png)

1. (Conditional) To add an additional environment, click the Plus icon and follow the instructions in this section.

1. (Conditional) To remove an existing environment, hover over the environment connection tab and click **X** when it appears.

   >[!WARNING]
   >
   >Removing a connection disconnects Fusion from that environment. The packages in it are no longer available in Fusion through that connection.

## Create and open a package

1. Click the **Packages** ![Packages icon](assets/packages-icon.png) tab in the left navigation panel.

1. Select the tab for the connection you want to work in.

1. Click **Create package**.

1. Enter a name and select **Create**.

   The package opens automatically.

1. To reopen a package later, select it from the Packages list and select **View**. 
1. To delete a package, select it from the Packages list and choose **Delete**.

   >[!WARNING]
   >
   >Deleting a package permanently removes it and everything inside it.

## Manage a package

An open package is organized into four areas:

* **Functions**: Create, test, and publish the function.
* **Variables**: Configure variables for the function.
* **Dependencies**: Install dependencies, such as outside libraries, for this function.
* **History**: View earlier versions of each function.

In addition to these four areas, a Storage meter at the top shows how much of your space is used. Each package has a total size limit of **21 MB**. This includes functions, variables, and dependencies, including saved versions. 

If you run out of space, we recommend removing unused dependencies, variables, or older versions to free some up.

To go back to the package list, select the back arrow next to the package name.

<!--Create toc here-->

### Functions

The **Functions** area displays a list of functions in the package, including the function's name, its status, its size, and how many inputs it expects. 

To filter the functions list:

1. Filter by status by clicking **All**, **Drafts**, or **Published**.
1. Use the search bar to search for specific functions.

#### Function status

A function can have the status of draft or published.

* **Draft**: Functions in Draft status are works in progress. You can edit and test freely without affecting live data.
* **Published**: Published versions are live. Your scenarios run published versions of functions. 

Using drafts allows you to safely make changes. You can refine a draft, test it, and then publish it when you are satisfied.

|Status|What it means|
|---|---|
|**Published**|A live version exists.|
|**Draft**|The function is still in progress, or a live function has changes you haven't published yet.|

#### Create or edit a function in the Packages area

1. Click the **Packages** ![Packages icon](assets/packages-icon.png) tab in the left navigation panel.1. In the **Functions** area, select **Create function**.

   Or

   Click the checkbox next to an existing function, and select **Edit** in the action bar at the bottom of the page.

1. If you are creating a new function, in the **New function** field, enter a name for the function.

1. On the **Code** tab, enter the function logic.

   Consider the following when creating your function:

   * Functions must be written in JavaScript.
   * You can read the inputs you define, reuse your variables, and call your other functions.
   * As you type, suggestions appear. 
   
1. To clean up function formatting, click **Beautify**.

1. (Optional) On the **Parameters** tab, define the inputs your function expects.

   For information on inputs, see [Define inputs](#define-inputs) in this article.

1. On the **Test** tab, test your function.

   For instructions, see [Test a function](#test-a-function) in this article.

1. To save this function as a draft, click **Save as draft**.

   Or

   To publish the function, click **Publish**.

   >[!NOTE]
   >
   >Publishing a function clears its version history. The published version becomes the current starting point, and earlier draft versions are no longer kept.

##### Define inputs

You can use the **Parameters** tab to describe the information your function needs each time it runs. 

1. Click the **Packages** ![Packages icon](assets/packages-icon.png) tab in the left navigation panel.1. In the **Functions** area, select **Create function**.

   Or

   Click the checkbox next to an existing function, and select **Edit** in the action bar at the bottom of the page.

1. Click the **Parameters** tab.

1. For each parameter you want to add, click **Add Parameter** and configure the following:

* **Name**: The name of the input
* **Label**: A user-friendly name shown when you test the function
* **Type**: The data type, such as text, number, true/false, or a structured object.
* **Required**: Whether a value must be provided.

These inputs become the fields you fill in when testing, and the values your scenario passes in when it runs the function.

##### Test a function

We recommend testing a function before publishing it.

1. Click the **Packages** ![Packages icon](assets/packages-icon.png) tab in the left navigation panel.1. In the **Functions** area, select **Create function**.

   Or

   Click the checkbox next to an existing function, and select **Edit** in the action bar at the bottom of the page.

1. Click the **Test** tab.

1. Enter a value for each input.

1. Run the function:

   * Select **Test Draft** to try your work-in-progress version.
   * Select **Execute Published** to run the live version.

1. Review the result, including whether it succeeded, how long it took, and the output it returned.

<!--start here-->

>[!NOTE]
>
>**Execute Published** is available only after a function has been published.

### Make changes to a live function

After a function is published, the **Publish** button becomes a menu:

* **Republish** — push your latest draft changes to the live version.
* **Unpublish** — take the function out of service. Your work is kept as a draft so you can come back to it.

#### Rename a function

Open the function, select the edit (pencil) icon next to its name, enter a new name, and select **Rename**. The new name applies everywhere, including past versions.

#### Delete a function

Select the function and choose **Delete**.

>[!WARNING]
>
>Deleting a function removes it completely, along with its history. Any scenario or function that uses it will stop working.

### Variables

Variables are reusable values—like a base URL, an account ID, or an API key—that your functions can use. Storing them as variables means you set a value once and update it in one place, instead of repeating it across many functions.

#### Create or edit a variable

1. On the **Variables** tab, select **New variable** (or **Edit** on an existing one).

1. Fill in the details:

   * **Key** — the name your functions use to refer to the value.
   * **Value** — the value to store.
   * **Type** — text, number, true/false, or a structured object.
   * **Description** — an optional note to remind you what it's for.
   * **Public** — turn this on to also use the variable in the scenario designer. When off, the variable is only available inside the package's functions.
   * **Secret** — turn this on to hide sensitive values (such as keys). The value is hidden in the variables list, and it's also kept out of sight in the scenario designer—its value is sanitized so it isn't exposed there. Your functions still receive the real value when they run.

1. Select **Create variable** or **Save changes**.

>[!NOTE]
>
>To rename a variable, change its **Key** while editing. Fusion replaces the old variable with a new one under the new name.

#### Delete a variable

Select the delete icon on a variable and confirm.

>[!WARNING]
>
>Functions that use a deleted variable will stop working.

## Use a package in a scenario

The point of building functions and variables is to put them to work in your scenarios. They become available in the scenario designer through the **Adobe App Builder** connector, which now includes two modules:

* **Use function from package** — run one of your functions as a step in a scenario. Choose the package and function, fill in the inputs you defined, and the function's result is passed along to the modules that follow.
* **Use variable from package** — bring one of your package variables into a scenario so you can map its value into other modules.

To add one:

1. In the scenario designer, add a module and choose the **Adobe App Builder** connector.

1. Select **Use function from package** or **Use variable from package**.

1. Choose the package and the function or variable you want, then map the inputs or value as needed.

>[!NOTE]
>
>Publish a function before using it in a scenario, and turn on **Public** for any variable you want to use there.

## Dependencies

Some functions need extra libraries to do their job. The **Dependencies** tab is where you add and manage those libraries.

### Add libraries

1. On the **Dependencies** tab, enter one or more library names, separated by commas. You can request a specific version by adding it after the name (for example, `axios, lodash@4.17.21`).

1. Select **Install**.

### Remove a library

Select the delete icon next to a library and confirm.

>[!WARNING]
>
>Functions that rely on a removed library may stop working.

## History

Every time you save a function, Fusion keeps a copy. The **History** tab lets you look back at earlier versions and bring one back if you need to.

* Select a function on the left to see its saved versions, newest first.
* Select a version to view exactly what it contained at that time.

This happens automatically—there's nothing to turn on. There's no set limit on how many versions are kept; they use part of your package's storage, so you can remove ones you no longer need.

>[!NOTE]
>
>Publishing a function clears its history. History tracks the changes you make while working on a draft, up until you publish.

### Restore an earlier version

Select a function, choose a version, and select **Restore as Draft**. That version comes back as a new draft, so you can review and test it before publishing. Your live version stays in place until you publish.

### Delete a version

Select a function and a version, then select **Delete Version** and confirm.

>[!WARNING]
>
>Deleting a version can't be undone.
