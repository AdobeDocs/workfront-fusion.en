---
title: "Frame.io (Beta) modules"
description: The [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] account.
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
---
# [!DNL Frame.io] V4 modules

>[!IMPORTANT]
>
>This article describes the new version of the Frame.io connector. This connector is used to connect to Frame.io version 4.
>
>For instructions on the legacy version of the Frame.io connector, see [Frame.io Legacy connector](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).

The Adobe Workfront Fusion [!DNL Frame.io] modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] account.

Workfront offers two Frame.io connectors, based on the version of Frame.io that you are connecting to.

| Connector | Frame.io version |
|---|---|
| Frame.io | V4 |
| Frame.io (Legacy) | V3 |

For instructions on the legacy version of the Frame.io connector, see [Frame.io Legacy connector](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


For a video introduction to the Frame.io connector, see:

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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
   <td role="rowheader">Adobe Workfront Fusion license</td> 
   <td>
   <p>Operation-based: No Workfront Fusion license requirement</p>
   <p>Connector-based (legacy): Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Prerequisites

To use [!DNL Frame.io] modules, you must have a [!DNL Frame.io] account

## Frame.io API information

The Frame.io connector uses the following:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Base URL</td> 
   <td> https://api.frame.io/v4</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API version</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API tag</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## Connect [!DNL Frame.io] to [!UICONTROL Adobe Workfront Fusion] 

You can connect automatically with user credentials, manually create a user credential connection, or create a server-to-server connection.

* [Connect automatically with user credentials](#connect-automatically-with-user-credentials#)
* [Create a user credentials connection manually](#create-a-user-credentials-connection-manually)
* [Create a server-to-server connection](#create-a-server-to-server-connection)

### Connect automatically with user credentials

This method creates a connection automatically if you are logged in to Frame.io, or connects you to the Frame.io login page so you can log in.

1. In any Frame.io Beta module, click **[!UICONTROL Add]** next to the Connection box.
1. Enter a name for the connection.
1. Click **Continue**.
1. If you are prompted to log in to your Frame.io account, do so.
1. If you are part of more than one Frame.io organization, select the organization that you want to use for this connection.

The connection is created.

### Create a user credentials connection manually

You can create a user credentials connection by logging into Frame.io, or by providing a Client ID or Client Secret.

To create a server-to-server connection, you must first configure an application in the Adobe Developer Console.

* [Create user credentials in the Adobe Developer Console](#create-user-credentials-in-the-adobe-developer-console)
* [Configure a user authentication connection](#configure-a-user-authentication-connection)

#### Create user credentials in the Adobe Developer Console

If you do not already have server-to-server credentials on an Adobe Developer Console project, you can create them.

1. Open the [Adobe Developer Console](https://developer.adobe.com/).
1. Select an existing project in the Adobe Developer Console to use for this connection

   Or
   
   Create a new project in the Adobe Developer Console. For instructions, see [Create an empty project](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. On the Project overview page or the Get started with your new project page, click **Add API**.
1. On the page that opens, locate and click **Frame.io API**.
1. On the Select authentication type page, select **User Authentication** and click **Next**.
1. On the Add a user authentication credential page, select **OAuth Web App** and click **Next**.
1. On the Configure OAuth Web App credential page, enter the following:   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Default redirect URI]</td>
          <td>
            <p><code>https://oauth.app.workfrontfusion.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Redirect URI pattern]</td>
          <td>
            <p><code>https://oauth\.app\.workfrontfusion\.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
       </tbody>
    </table>
1. Click **Next**.
1. Click **Save configured API**.
1. On the product page, click the card for the credentials you just created. 

   Here, you can find your Client ID and Client Secret.

>[!NOTE]
>
> We recommend leaving this window open as you begin configuring your connection in Adobe Workfront Fusion. You can copy the Client ID, and retrieve and copy Client Secret from this page to paste into the connection fields. 


#### Configure a user authentication connection

1. In any  Frame.io Beta module, click **[!UICONTROL Add]** next to the Connection box.
1. In the Create a connection box, click **Show advanced settings**.

1. Fill in the following fields:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>Select <b>IMS User authentication</b>.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Enter a name for this connection.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Enter your [!DNL Adobe] [!UICONTROL Client ID]. This can be found in the [!UICONTROL Credentials details] section of the [!DNL Adobe Developer Console].<p>For instructions on creating credentials, see <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Create user credentials in the Adobe Developer Console</a> in this article.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Enter your [!DNL Adobe] [!UICONTROL Client Secret]. This can be found in the [!UICONTROL Credentials details] section of the [!DNL Adobe Developer Console].<p>For instructions on creating credentials, see <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Create user credentials in the Adobe Developer Console</a> in this article.</p>
        </tr>
       </tbody>
    </table>
1. If you are prompted to log in to your Frame.io account, do so.
1. If you are part of more than one Frame.io organization, select the organization that you want to use for this connection.

The connection is created.


### Create a server-to-server connection

To create a server-to-server connection, you must first configure an application in the Adobe Developer Console.

* [Create server-to-server credentials in the Adobe Developer Console](#create-server-to-server-credentials-in-the-adobe-developer-console)
* [Configure a server-to-server connection](#configure-a-server-to-server-connection)

#### Create server-to-server credentials in the Adobe Developer Console

If you do not already have server-to-server credentials on an Adobe Developer Console project, you can create them.

1. Open the [Adobe Developer Console](https://developer.adobe.com/).
1. Select an existing project in the Adobe Developer Console to use for this connection

   Or
   
   Create a new project in the Adobe Developer Console. For instructions, see [Create an empty project](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. On the Project overview page or the Get started with your new project page, click **Add API**.
1. On the page that opens, locate and click **Frame.io API**.
1. On the Select authentication type page, select **Server-to-Server Authentication** and click **Next**.
1. Enter a name for the credentials. This allows you to identify the credentials later in the API Credentials area of the Adobe Admin Console.
1. Click **Next**.
1. On the Select product profiles page, select the product profile that includes the Frame.io account that you want to connect to.
1. Click **Save configured API**.
1. On the product page, click the card for the credentials you just created. 

   Here, you can find your Client ID and Client Secret.

>[!NOTE]
>
> We recommend leaving this window open as you begin configuring your connection in Adobe Workfront Fusion. You can copy the Client ID, and retrieve and copy Client Secret from this page to paste into the connection fields. 


#### Configure a server-to-server connection

1. In any  Frame.io Beta module, click **[!UICONTROL Add]** next to the Connection box.

1. Fill in the following fields:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>Select <b>IMS Server to Server</b>.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Enter a name for this connection.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Enter your [!DNL Adobe] [!UICONTROL Client ID]. This can be found in the [!UICONTROL Credentials details] section of the [!DNL Adobe Developer Console].<p>For instructions on creating credentials, see <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Create server-to-server credentials in the Adobe Developer Console</a> in this article.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Enter your [!DNL Adobe] [!UICONTROL Client Secret]. This can be found in the [!UICONTROL Credentials details] section of the [!DNL Adobe Developer Console].<p>For instructions on creating credentials, see <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Create server-to-server credentials in the Adobe Developer Console</a> in this article.</p>
        </tr>
       </tbody>
    </table>
1. Click **[!UICONTROL Continue]** to save the connection and return to the module.




## [!DNL Frame.io] modules and their fields

When you configure [!DNL Frame.io] modules, Workfront Fusion displays the fields listed below. Along with these, additional [!DNL Frame.io] fields might display, depending on factors such as your access level in the app or service. A bolded title in a module indicates a required field.

If you see the map button above a field or function, you can use it to set variables and functions for that field. For more information, see [Map information from one module to another](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Map toggle](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Assets](#assets)
* [Comments](#comments)
* [Folders](#folders)
* [Projects](#projects)
* [Shares](#shares)
* [Workspaces](#workspaces)
* [Other](#other)

### Assets 

* [[!UICONTROL Create an asset]](#create-an-asset)
* [[!UICONTROL Delete an asset]](#delete-an-asset)
* [[!UICONTROL Get an asset]](#get-an-asset)
* [[!UICONTROL List assets]](#list-assets)
* [Watch asset deleted](#watch-asset-deleted)
* [Watch new asset](#watch-new-asset)

#### [!UICONTROL Create an asset] <!--different for v4-->

This action module creates a new asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account that contains the project that you want to create an asset for.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Select the workspace or map the ID of the workspace that contains the project that you want to create an asset for.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Select the project or map the ID of the project that you want to create an asset for.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Select the path where you want to create an asset.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td> <p>Enter the name of the file that you want to use for this asset.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">File Size </td> 
    <td> <p>Enter or map the file size in bytes.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>If creating a file, enter the URL of the file you want to upload.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>Select the media type for this asset.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL Delete an asset] 

This action module deletes a specified asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account that contains the asset that you want to delete.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Select or map the asset you want to delete.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an asset]

This action module retrieves asset details.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account that contains the asset that you want to retrieve.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Select or map the asset you want to retrieve.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List assets]

This search module retrieves all assets in the specified project's folder.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account that contains the assets that you want to list.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned assets] </td> 
   <td> <p>Enter or map the maximum number of assets you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Watch asset deleted

This trigger module starts a scenario when an asset is deleted.

Select the webhook that you want to use for this module, or click Add next to the Webhook field and enter the following information:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Enter a name for the new webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account you want to watch for deleted assets.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Watch new asset

This trigger module starts a scenario when a new asset is created.

Select the webhook that you want to use for this module, or click Add next to the Webhook field and enter the following information:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Enter a name for the new webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account you want to watch for new assets.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Comments 

* [[!UICONTROL Create a Comment]](#create-a-comment)
* [[!UICONTROL Delete a Comment]](#delete-a-comment)
* [[!UICONTROL Get a Comment]](#get-a-comment)
* [[!UICONTROL List Comments]](#list-comments)
* [[!UICONTROL Update a Comment]](#update-a-comment)
* [Watch comment updated](#watch-comment-updated)
* [Watch new comment](#watch-new-comment)

#### [!UICONTROL Create a comment]

This action module adds a new comment or reply to the asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account that contains the asset you want to add a comment to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Select the account or map the ID of the workspace that contains the asset you want to add a comment to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Select the project or map the ID of the project that contains the asset you want to add a comment to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Select the path to the asset that you want to add a comment to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Enter the text content of the comment or reply.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Enter the frame number in the video the comment should be linked to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page] </td> 
   <td> <p>If the asset is a PDF, enter or map the page that the comment should be attached to.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a comment]

This action module deletes an existing comment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account that contains comment that you want to delete.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Enter or map the ID of the comment you want to delete.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a comment]

This action module retrieves details of the specified comment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account that contains comment that you want to retrieve details about.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Select the comment you want to retrieve details about.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List comments]

This search module retrieves all comments of the specified asset.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select or map the account that contains the asset that you want to retrieve comments from.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Select or map the workspace that contains the asset that you want to retrieve comments from.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Select the project that contains the asset you want to retrieve comments from.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Select the the path that leads to the asset you want to list comments from.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments] </td> 
   <td> <p>Enter or map the maximum number of comments you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a comment]

This action module edits an existing comment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select or map the account that contains the project that contains the asset you want to update a comment on.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Select the comment you want to update.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Enter the text content of the comment.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Enter the frame number in the video the comment is linked to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page] </td> 
   <td> <p>If the asset is a PDF, enter or map the page that the comment is attached to.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Watch comment updated

This trigger module starts a scenario when a comment is updated.

Select the webhook that you want to use for this module, or click Add next to the Webhook field and enter the following information:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Enter a name for the new webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account you want to watch for updated comments.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Watch new comment

This trigger module starts a scenario when a comment is created.

Select the webhook that you want to use for this module, or click Add next to the Webhook field and enter the following information:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Enter a name for the new webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account you want to watch for new comments.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Folders

#### Create a folder

This action module creates a new folder in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select or map the account where you want to create a folder.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Select or map the workspace where you want to create a folder.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Select the where you want to create a folder.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Select the the path where you want to create a folder.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Enter or map a name for the new folder.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projects

* [Create a project](#create-a-project)
* [Invite users to Frame.io Project](#invite-users-to-frameio-project)
* [List projects](#list-projects)

#### Create a project

This action module creates a new project in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select or map the account where you want to create a project.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Select or map the workspace where you want to create a project.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Enter or map a name for the new project.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Invite users to Frame.io Project

This action module invites users to the specified Frame.io project.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select or map the account that contains the project you want to invite a user to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Select or map the workspace contains the project you want to invite a user to.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Project ID </td> 
   <td> <p>Select or map the project that you want to invite a  user to.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">User ID </td> 
   <td> <p>Select or map the user that you want to invite to the project.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Projects]

This search module retrieves all projects for the specified team.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select or map the account that contains the asset that you want to retrieve projects from.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Select or map the workspace that contains the asset that you want to retrieve projects from.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned projects] </td> 
   <td> <p>Enter or map the maximum number of projects
   you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Shares

* [Add an asset to a share link](#add-an-asset-to-a-share-link)
* [Create a share link](#create-a-share-link)

#### Add an asset to a share link

This action modules adds an asset to a share link in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select or map the account that contains the share link that you want to add an asset to.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share link ID] </td> 
   <td> <p>Select or map the share link that you want to add an asset to.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Enter or map ID of the asset that you want to add to the share link.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Create a share link

 This action module creates a new share link in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select or map the account where you want to create a share link.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Select or map the workspace where you want to create a share link.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Select or map the project where you want to create a share link.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Access </td> 
   <td> <p>Select whether this link has public or restricted access.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Assets </td> 
   <td> <p>For each asset that you want to add to the share link, click <b>Add item</b> and enter the asset's ID.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Description </td> 
   <td> <p>Enter or map a description for the share link.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Enter or map the expiration date for the share link.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Enter or map a name for the new share link.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Name </td> 
   <td> <p>Enter or map a passphrase for the share link.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Workspaces

#### Create a workspace

This action module creates a new workspace in Frame.io

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select or map the account where you want to create a workspace.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Enter or map a new name for the workspace.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### List workspaces

This module lists all workspaces in an account.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select or map the account that contains the asset that you want to retrieve workspaces from.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned workspaces] </td> 
   <td> <p>Enter or map the maximum number of workspaces
   you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Other

* [Make a custom API call](#make-a-custom-api-call)
* [Watch metadata value updated](#watch-metadata-value-updated)


#### [!UICONTROL Make a custom API call]

This module allows you to perform a custom API call.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Enter a path relative to <code>https://api.frame.io</code>. Example: <code> /v4/me</code></p> <p>Note: For the list of available endpoints, refer to the [!DNL Frame.io] API Reference.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Select the HTTP request method you need to configure the API call. For more information, see <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP request methods</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Add the headers of the request in the form of a standard JSON object.</p> <p>For example, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion adds authorization headers automatically.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query string] </td> 
   <td> <p>Enter the request query string. For each parameter that you want to include in the query string, click <b>[!UICONTROL Add item]</b> and enter the field's name and the desired value.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Add the body content for the API call in the form of a standard JSON object.</p> <p>Note:  <p>When using conditional statements such as <code>if</code> in your JSON, put the quotation marks outside of the conditional statement.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Watch metadata value updated

This trigger module starts a scenario when a comment is updated.

Select the webhook that you want to use for this module, or click Add next to the Webhook field and enter the following information:

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Enter a name for the new webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>For instructions on creating a connection to [!DNL Frame.io], see <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connect [!DNL Frame.io] to Adobe Workfront Fusion</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Select the account or map the ID of the account you want to watch for updated metadata values.</p> </td> 
  </tr> 
 </tbody> 
</table>


<!-- 
**Example:** The following API call returns all teams and its details in your [!DNL Frame.io] account:

URL: `/v2/teams`

Method: `GET`

![API call example](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![API call output](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
