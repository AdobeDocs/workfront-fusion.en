---
title: HTTP request methods
description: When you are configuring an API call in a module, you must select the HTTP request method. This article describes the available methods, and why you would select each one.
author: Becky
feature: Workfront Fusion
---
# HTTP request methods

When you are configuring an API call in a module, you must select the HTTP request method. This article describes the available methods, and why you would select each one.

## HTTP methods

Use one of the following HTTP methods.

* **[!UICONTROL GET]**: Retrieves data from a web server based on your parameters. [!UICONTROL GET] requests a representation of the specified resource, and receives a [!UICONTROL 200 OK] response message with the requested content if successful.
* **[!UICONTROL POST]**: Sends data to a web server based on your parameters. [!UICONTROL POST] requests include actions like uploading a file. Multiple [!UICONTROL POST]s may result in a different outcome than a single [!UICONTROL POST], so be cautious about unintentionally sending multiple [!UICONTROL POST]s. If a [!UICONTROL POST] is successful, you receive a [!UICONTROL 200 OK] response message.
* **[!UICONTROL PUT]**: Sends data to a location in the web server based on your parameters. [!UICONTROL PUT] requests include actions like uploading a file. The difference between a [!UICONTROL PUT] and [!UICONTROL POST] is that PUT is idempotent, meaning that the result of a single successful [!UICONTROL PUT] is the same as many identical [!UICONTROL PUT]s. If a PUT is successful, you receive a 200 response message (usually 201 or 204).
* **[!UICONTROL PATCH]**: (Not available for some API call modules) Applies partial modifications to a resource on a web server based on your parameters. [!UICONTROL PATCH] is not idempotent, meaning that the result of multiple [!UICONTROL PATCH]'s could have unintended consequences. If a [!UICONTROL PATCH] is successful, you will receive a 200 response message (usually 204).
* **[!UICONTROL DELETE]**: Deletes the specified resource from the web server based on your parameters (if the resource exists). If a [!UICONTROL DELETE] is successful, you receive a 200 OK response message.
