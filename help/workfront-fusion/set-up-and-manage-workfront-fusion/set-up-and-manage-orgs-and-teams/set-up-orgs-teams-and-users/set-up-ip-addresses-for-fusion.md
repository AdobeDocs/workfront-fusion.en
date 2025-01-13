---
title: Configure IP Addresses for Fusion in your organization's allowlist
description: Fusion uses specific IP addresses and domains for web communication. These must be added to your organization's allowlist before you can use Workfront in your organization.
author: Becky
feature: Workfront Fusion
exl-id: 406dd45c-0863-4270-a80e-c1c115e0b367
---
# Configure IP Addresses for Fusion in your organization's allowlist

Because Adobe Workfront Fusion communicates with your organization's network, your organization's firewall must be configured to allow that communication. Firewalls are highly effective security measures that function by separating an organization's network from the internet. They ensure that only selected data and network traffic can move into or out of the organization's network. The firewall allows or blocks data based on the site that is sending or receiving the data. As a Fusion administrator, you must ensure that data sent to or from Fusion can pass through your organization's firewall.

This is accomplished through an allowlist, which is essentially a "list" of sites that are "allowed" to send or receive data through the firewall. Sites can be identified in one of two ways:

* **IP address**: a series of numbers such as 52.31.132.175
* **Domain**: part of a URL, such as `thisdomain` in `www.thisdomain.com`

Fusion uses specific IP addresses and domains for web communication. These must be added to your organization's allowlist before you can use Workfront in your organization.

Usually, an allowlist is configured by a network administrator. Work with your organization's network administrator to ensure that your firewall allows these IP addresses. If you do not know who your network administrator is, your organization's IT department can point you in the right direction.

>[!IMPORTANT]
>
>As a Fusion administrator, you must ensure that these IP addresses and domains are added to your organization's allowlist. This is true even if you do not add them yourself. Fusion cannot configure your organization's allowlist.

You can add all Fusion IP addresses and domains to your allowlist, or you can locate your Fusion cluster and add only the IP addresses and domains for that cluster.

## Add all Fusion IP addresses and domains

Add the following IP addresses to your allowlist:

* 52.30.133.50
* 54.220.93.204 
* 34.254.76.122
* 54.244.142.219 
* 52.39.217.230 
* 44.241.82.96
* 100.20.126.137
* 34.223.32.4
* 52.39.176.220
* 20.36.133.48/28 
* 20.81.156.240/28 
* 172.172.84.48/28 

Also, if your organization uses outbound network filtering, add the following domain to your allowlist to enable your system to access Workfront Fusion.

* hook.app.workfrontfusion.com
* hook.app-eu.workfrontfusion.com
* hook.app-az.workfrontfusion.com

## Add Fusion IP addresses and domains for your cluster only

### Identify your datacenter

The IP addresses vary based on where your data is stored. 

If you access Fusion through a URL, you can examine the URL to locate your datacenter.

| URL | Datacenter |
| --- | --- |
| `https://app.workfrontfusion.com` | US datacenter |
| `https://app-eu.workfrontfusion.com` | EU datacenter |
| `https://app-az.workfrontfusion.com` | Azure cluster |

If you access Fusion through `experience.adobe.com`, you can check the network tab in your browser to identify the datacenter.

| URL | Datacenter |
| --- | --- |
| Calls to `https://fusion.adobe.com` |US datacenter |
| Calls to `https://eu.fusion.adobe.com` | EU datacenter |
| Calls to `https://az.fusion.adobe.com`  | Azure cluster |

### Add IP addresses and domains for your datacenter

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] EU Datacenter</td> 
   <td> 
    <ul> 
     <li>52.30.133.50</li> 
     <li>54.220.93.204</li> 
     <li>34.254.76.122</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront] US Datacenter</p> </td> 
   <td> 
    <ul> 
     <li>54.244.142.219</li> 
     <li>52.39.217.230</li> 
     <li>44.241.82.96</li>
     <li>100.20.126.137</li>
     <li>34.223.32.4</li>
     <li>52.39.176.220</li>
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] on the Microsoft Azure cluster</td> 
   <td> 
    <ul> 
     <li>20.36.133.48/28</li> 
     <li>20.81.156.240/28</li> 
     <li>172.172.84.48/28</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Also, if your organization uses outbound network filtering, add the following domain to your allowlist to enable your system to access Workfront Fusion. These are used for webhooks

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] EU Datacenter</td> 
   <td> <p> hook.app-eu.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront] US Datacenter</p> </td> 
   <td> <p>hook.app.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront Fusion] on the Microsoft Azure cluster</p> </td> 
   <td> <p>hook.app-az.workfrontfusion.com </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Outbound network filtering is uncommon. Check with your network administrator to see if you need to update your allowlist to accommodate for it.
