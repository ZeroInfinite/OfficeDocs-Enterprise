---
title: "Retrieve customer tenant reporting data with Windows PowerShell for Delegated Access Permissions (DAP) partners"
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 12/15/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: 
ms.assetid: 893e5275-30b3-433f-8ecd-644f78f513e2
description: "Summary: Use remoteWindows PowerShell for Microsoft Exchange Online to retrieve reports from individual customer tenants."
---

# Retrieve customer tenant reporting data with Windows PowerShell for Delegated Access Permissions (DAP) partners

 **Summary:** Use remoteWindows PowerShell for Microsoft Exchange Online to retrieve reports from individual customer tenants.
  
Syndication and Cloud Solution Provider (CSP) partners can access the data that makes up customer tenant reports directly via remoteWindows PowerShell for Exchange Online PowerShell. This lets partners collect and save the reporting data and then perform other operations on it. After you open a remote connection, retrieving reporting data about a customer tenancy is identical to running any cmdlet against a customer tenancy.
  
In this article, you use remoteWindows PowerShell for Exchange Online to connect to a single customer tenancy and retrieve a report. By default, Windows PowerShell does not support aggregating reporting data from multiple customer tenancies. The reports you retrieve with this procedure are only for the  _DelegatedOrg_ that you connect to.
  
If you want to retrieve a single report for all your customer tenancies, a sample script to do this can be found in [Aggregate customer reporting data via Windows PowerShell for Delegated Access Permission (DAP) partners](aggregate-customer-reporting-data-via-windows-powershell-for-delegated-access-pe.md) .
  
## Before you begin

- You need to connect to your Exchange Online tenant by using remote Windows PowerShell. For instructions, see [Connect to Exchange Online tenants with remote Windows PowerShell for Delegated Access Permissions (DAP) partners](connect-to-exchange-online-tenants-with-remote-windows-powershell-for-delegated.md)
    
## Run the Get-StaleMailboxReport sample

After you have opened a remote session to Exchange Online, run this command to retrieve the **Get-StaleMailboxReport** for the date range 03/25/2015 through 03/31/2015.
  
```
Get-StaleMailboxReport -StartDate 03/25/2015 -EndDate 03/31/2015
```

There are many other reporting cmdlets available for Exchange Online, Lync Online, and SharePoint Online as well as others for message tracing that you can use. To find out more about the available reporting cmdlets and the Office 365 Reporting web service, see the topics in the following section.
  
## See also

#### 

[Office 365 Reporting web service](https://go.microsoft.com/fwlink/p/?LinkId=532777)
  
[Reporting cmdlets in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=526430)
  
[Help for partners](https://go.microsoft.com/fwlink/p/?LinkID=533477)

