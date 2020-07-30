---
title: Aspose.Email for .NET 17.8 Release Notes
type: docs
weight: 50
url: /net/aspose-email-for-net-17-8-release-notes/
---

{{% alert color="primary" %}} 

This page contains release notes for Aspose.Email for .NET 17.8 release.

{{% /alert %}} 
## **Features and Improvements**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|EMAILNET-38782|Ability to [save images inside a message (as embedded image) as separate files](/email/net/loading-and-saving-message/#loadingandsavingmessage-savingashtmlwithoutembeddingresources) next to html file while converting MSG to HTML|Enhancement|
|EMAILNET-38635|Add support Exchange 2016|Enhancement|
|EMAILNET-38773|Smtp functionality with System.Threading|Bug|
|EMAILNET-38779|EML to MSG results in malformed output|Bug|
|EMAILNET-38781|PDF attachment can't be recognized from attachments|Bug|
|EMAILNET-38785|Attachments not recognized in MSG file|Bug|
|EMAILNET-38794|Timezone property for recurrence|Bug|
|EMAILNET-38796|Fetch PST properties PR_LAST_VERB_EXECUTED and PR_CALENDAR_MEETING_STATUS|Bug|
|EMAILNET-38792|Pop3.FetchMessage raises exception with FIPS compliant environment|Bug|

### **Added APIs**
Class Aspose.Email.SaveResourceHandler
Field/Enum Aspose.Email.Mapi.MapiPropertyTag.PR_LAST_VERB_EXECUTED
Method Aspose.Email.Clients.Exchange.WebService.EWSClient.FolderTypeToFolderClass(ExchangeFolderType)
Method Aspose.Email.Clients.Exchange.WebService.IEWSClient.CreateFolder(String, ExchangeFolderType)
Method Aspose.Email.Clients.Exchange.WebService.IEWSClient.CreateFolder(String, String, ExchangeFolderType)
Method Aspose.Email.Clients.Exchange.WebService.IEWSClient.CreatePublicFolder(String, ExchangeFolderPermissionCollection, ExchangeFolderType)
Property Aspose.Email.HtmlSaveOptions.SaveResourceHandler
