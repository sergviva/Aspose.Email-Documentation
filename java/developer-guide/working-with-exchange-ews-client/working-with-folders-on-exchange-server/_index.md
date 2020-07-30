---
title: Working with Folders on Exchange Server
type: docs
weight: 100
url: /java/working-with-folders-on-exchange-server/
---

{{% alert color="primary" %}} 

Aspose.Email API provides the capability to connect to the Exchange Server and list all the folders and sub-folders. You can also retrieve all the sub-folders from each folder recursively. It also provides the capability to enumerate folders with paging from the Exchange client using Exchange Web Serice (EWS). This article shows how to retrieve all the sub-folders from the Exchange server and retrieve folders with pagination.

{{% /alert %}} 
## **Listing Folders**
### **List Folders from Exchange Server**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ListAllFolders-.java" >}}
### **List Folders with Paging Support**
For a large number of folders on Exchange Server, it might not be convenient to retrieve all the folders list at once. Aspose.Email for Java API lets you list folders from the Exchange server with paging support. The following example demonstrates the usage of this API feature.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ListingFoldersWithPagingSupport-.java" >}}
## **Getting Folder Type Information using EWS**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchangeews-GetFolderTypeInformationUsingEWS-GetFolderTypeInformationUsingEWS.java" >}}
## **Creating Folders and Sub-Folders using EWS**
{{% alert color="primary" %}} 

Aspose.Email API provides the capability to create folders in an Exchange mailbox. The [CreateFolder](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#createFolder\(java.lang.String\)) method of [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) can be used for this purpose.

{{% /alert %}} 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-CreateFolders-.java" >}}
## **Synchronizing Folder Items using EWS**
{{% alert color="primary" %}} 

Aspose.Email for Java API's [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) provides the feature of syncing an Exchange folder for its contents. The [SyncFolder](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#syncFolder\(java.lang.String\)) method exposed by the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) class can be used to perform folder sync information on a specified folder. The following code sample demonstrates the usage of syncing Exchange folder information.

{{% /alert %}} 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-SynchronizeFolderItems-.java" >}}
## **Access Mailbox Custom Folders or Subfolders**
{{% alert color="primary" %}} 

[IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) lets developers access any custom folder or subfolder from the mailbox. The [folderExists()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#folderExists\(java.lang.String,%20java.lang.String\)) function of [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) returns the URI of a specified custom folder/sub-folder, which can be used then to access the target folder.

{{% /alert %}} 

In the following example, a custom folder named "TestInbox", which is created under INBOX is accessed and all the messages are displayed from this custom folder.

To perform this task, the following are the steps:

1. Initialize the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) object by providing valid credentials.
1. Access the default mailbox.
1. Access the parent folder, which is INBOX in this example. This parent folder can also be a custom folder itself.
1. Use [folderExists()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#folderExists\(java.lang.String,%20java.lang.String\)) to search the specified custom subfolder, for example "TestInbox". It will return the URI of "TestInbox".
1. Use this Uri to access all the messages in that custom folder.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-AccessMailboxCustomFoldersOrSubfolders-.java" >}}
## **Retrieve Folder Permissions using EWS Client**
{{% alert color="primary" %}} 

Users are assigned permissions to public folders on Exchange Server, which limits/determine the level of access a user has to these folders. The [ExchangeFolderPermission](https://apireference.aspose.com/java/email/com.aspose.email/ExchangeFolderPermission) class provides a set of permission properties for Exchange folders such as the permission level, whether they can create items, deleting items, and perform other tasks as specified by the permission properties. Permissions can be retrieved using the [getFolderPermisssions()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#getFolderPermissions\(java.lang.String\)) method of [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient).

This article shows how to retrieve the permissions applied to a public folder for all the users who have access to the shared folders.

{{% /alert %}} 


The following example shows how to use the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class to retrieve permissions applied to a folder.

To perform this task:

1. Initialize the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient).
1. Use the [listPublicFolders()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#listPublicFolders\(\)) to get a list of all public folders.
1. Retrieve the permissions associated with a folder using the [getFolderPermissions()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#getFolderPermissions\(java.lang.String\)) method.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-RetrievePermissionsForExchangeFolders-.java" >}}
## **Download Messages from Public Folders of Exchange Server**
{{% alert color="primary" %}} 

Microsoft Exchange Server lets users create public folders and post messages in them. To do this through your application, use Aspose.Email's [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class to connect to the Exchange Server and read and download messages and posts from public folders.

{{% /alert %}} 

The sample source code below reads all public folders, and subfolders, and lists and downloads any messages found in these folders. This example only works with Microsoft Exchange Server 2007 or above since only these support EWS.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-DownloadMessagesFromPublicFolders-.java" >}}
## **Backup Exchange Folders to PST**
{{% alert color="primary" %}} 

It often so happens that users may want to take a backup of all or some of the mailbox folders. Aspose.Email provides the capability to take the backup of all or specified Exchange mailbox folders to a PST. This article describes taking backup of Exchange folders to a PST with sample code.

{{% /alert %}} 

In order to take a backup of Exchange server folders, the following steps may be followed.

1. Initiate the Exchange Web Service (EWS) client with user credentials.
1. Add the required folder's info to [ExchangeFolderInfoCollection](https://apireference.aspose.com/java/email/com.aspose.email/ExchangeFolderInfoCollection).
1. User the client's [Backup](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#backup\(com.aspose.email.ExchangeFolderInfoCollection,%20java.io.OutputStream,%20int\)) method to export the folder's contents to PST.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-BackupExchangeFoldersToPST-.java" >}}
