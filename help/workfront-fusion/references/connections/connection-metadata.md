---
title: Connection metadata
description: Fusion uses metadata to identify important attributes of a connection.
author: Becky
feature: Workfront Fusion
exl-id: b41fbe8c-30fa-49d0-8a24-3535642b97ae
---
# Connection metadata

Fusion uses metadata to identify important attributes of a connection.  

Connection metadata can be set when creating a new connection. These attributes are in the same dialog box used for setting up a connection: 

![Connection metadata](assets/connection-metadata-setup.png)

Fusion users can view and edit connections from the Connections area.  

![Connection metadata in Connections area](assets/connections-area-metadata.png)

## Environment Type 

Fusion connections can be used by both production and non-production systems. You can mark the type of environment a connection connects to, which helps protect production environments. 

The environment type, like other connection metadata, is used for informational purposes only. Users are responsible for accurately setting this attribute, and using a connection with the correct environment in a scenario. 

## Authentication Type 

Fusion connections can be used for both service accounts and personal accounts. Service accounts are used for authentication when a scenario automates as Fusion. Personal accounts are authentication based on a specific person. Which authentication type is used depends on the scenario's requirements. Personal accounts should be used for automated user actions. For example, if a Fusion scenario automates approval by a specific person, then the authentication type should be for that person. Otherwise, Fusion is acting as Fusion and the type should be Service Account.

Authentication type, like other connection metadata, is used for informational purposes only. Users are responsible for accurately setting this attribute, and using the correct type of connection in a scenario.

For more information on authentication types, please see [Authentication](https://developer.adobe.com/developer-console/docs/guides/authentication/) in Adobe's Authentication guide.

## Resources

* For instructions on managing connection metadata, see [Manage connections](/help/workfront-fusion/create-scenarios/connect-to-apps/manage-connections.md).
