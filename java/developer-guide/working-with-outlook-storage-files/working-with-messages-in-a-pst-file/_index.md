---
title: Working with Messages in a PST File
type: docs
weight: 30
url: /java/working-with-messages-in-a-pst-file/
---

## **Get the Messages Information from the Outlook PST File**
[Read Outlook PST File and Get Folders and Subfolders Information](/java/read-outlook-pst-file-and-get-folders-and-subfolders-information/) discussed how to load an Outlook PST file and browse its folders to get folder names and the number of messages in each folder. This article explains how to read all the folders and subfolders in the PST file and display the information about messages, for example, subject, sender, recipients, and so on.

The Outlook PST file can contain nested folders. Use a recursive method to read all the folders (including nested folders). Below is the complete code of a console application that reads an Outlook PST file and displays the folder and message contents recursively.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-GetMessageInformationFromPSTFile-.java" >}}
## **Extract Messages from Outlook PST File and Save to Disk or Stream in MSG Format**
This article shows how to read an Outlook PST file, extract messages and save them to disk in MSG format.
### **Extract and Save Messages**
The task is achieved by using a recursive method to browse through all the folders (including nested folders) and calling the PersonalStorage.extractMessage() method to get Outlook messages in an instance of the [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) class. After that, the [MapiMessage.save()](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage#save\(java.io.OutputStream\)) method is called to save the message in MSG format to either disk or stream.

The complete source code of a console application for extracting messages from PST file is given below.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-PSTExtractMessages-.java" >}}
### **Save Messages Directly from PST to Stream**
In order to save messages from PST directly to a stream, without extracting [MessageInfo](https://apireference.aspose.com/java/email/com.aspose.email/messageinfo) for messages, the [saveMessageToStream()](https://apireference.aspose.com/java/email/com.aspose.email/PersonalStorage#saveMessageToStream\(java.lang.String,%20java.io.OutputStream\)) method can be used as follows:

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-SaveMessageDirectlyFromPSTToStream-SaveMessageFromPSTToStream1.java" >}}

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-SaveMessageDirectlyFromPSTToStream-SaveMessageFromPSTToStream2.java" >}}

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-SaveMessageDirectlyFromPSTToStream-SaveMessageFromPSTToStream3.java" >}}
### **Extract n Messages from a PST File**
The following code sample shows how to extract a given number of messages from a PST. Simply provide the index for the first message, and the total number of messages to be extracted.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-ExtractingNMessagesFromAPSTFile-.java" >}}
## **Delete Messages from PST**
It is possible to delete items (contents) from a PST file by using the FolderInfo.deleteChildItem() method. It may also be desirable to delete messages in bulk. Items from a PST file can be deleted using the FolderInfo.deleteChildItem() method. The API also provides [FolderInfo.deleteChildItems()](https://apireference.aspose.com/java/email/com.aspose.email/FolderInfo#deleteChildItems\(java.lang.Iterable\)) method to delete items in bulk from the PST file.
### **Delete Items from PST One by One**
The example below uses the [FolderInfo](https://apireference.aspose.com/java/email/com.aspose.email/folderinfo) class to access any specific folder from PST. Below are the steps to delete messages from the Sent sub-folder of a previously loaded or created PST file:

1. Create an instance of the [FolderInfo](https://apireference.aspose.com/java/email/com.aspose.email/folderinfo) class and load it with the contents of the Sent sub-folder using the [PersonalStorage.getPredefinedFolder](https://apireference.aspose.com/java/email/com.aspose.email/PersonalStorage#getPredefinedFolder\(int\)) method.
1. Delete messages from the Sent folder by calling the FolderInfo.deleteChildItem() method and passing the [MessageInfo.EntryId](https://apireference.aspose.com/java/email/com.aspose.email/MessageInfo#getEntryId\(\)) as a parameter.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-DeleteMessagesFromPST-DeleteItemsFromPSTOneByOne.java" >}}
### **Delete Items in Bulk from PST File**
Aspose.Email API can be used to delete items in bulk from a PST file. This is achieved using the [deleteChildItems](https://apireference.aspose.com/java/email/com.aspose.email/FolderInfo#deleteChildItems\(java.lang.Iterable\)) method which accepts a list of Entry ID items referring to the items to be deleted.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-DeleteMessagesFromPST-DeleteItemsInBulkFromPSTFile.java" >}}
## **Search Messages and Folders in a PST by Some Criteria**
Personal Storage (PST) files can contain a huge amount of data and searching for data that meets a specific criteria in such large files needs to include multiple checkpoints in the code to filter the information. With the [MailQueryBuilder](https://apireference.aspose.com/java/email/com.aspose.email/MailQueryBuilder) class, Aspose.Email makes it possible to search for specific records in a PST based on specified search criteria. A PST can be searched for messages based on search parameters such as sender, receiver, subject, message importance, presence of attachments, message size, and even message ID. The [MailQueryBuilder](https://apireference.aspose.com/java/email/com.aspose.email/MailQueryBuilder) can also be used to search for subfolders.
### **Search Messages and Folders in PST**
The following code sample shows how to use the [MailQueryBuilder](https://apireference.aspose.com/java/email/com.aspose.email/MailQueryBuilder) class to search for content in a PST based on different search criteria. For example, it shows searching a PST based on:

- Message importance.
- Message class.
- Presence of attachments.
- Message size.
- Unread messages.
- Unread messages with attachments, and
- folders with a specific subfolder name.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-StringSearchingInPSTWithIgnoreCase-.java" >}}
## **Move Items to Other Folders in a PST**
Aspose.Email makes it possible to move items from a source folder to another folder in the same Personal Storage (PST) file. This includes:

- Moving a specified folder to a new parent folder.
- Moving a specified message to a new folder.
- Moving the contents to a new folder.
- Moving subfolders to a new parent folder.

The following code sample shows how to move items such as messages and folders from a source folder to another folder in the same PST file.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-MoveItemsToOtherFoldersInAPST-.java" >}}
## **Updating Message Properties in PST File**
It's sometimes required to update certain properties of messages such as changing the subject, marking message importance and similarly others. Updating a message in a PST file, with such changes in the message properties, can be achieved using the [FolderInfo.changeMessages](https://apireference.aspose.com/java/email/com.aspose.email/FolderInfo#changeMessages\(java.lang.Iterable,%20com.aspose.email.MapiPropertyCollection\)) method. This article shows how to update messages in bulk in a PST file for changes in the properties.
### **Update Messages in Bulk in PST file**
The following code sample shows how to update properties of messages in bulk mode for multiple messages in a PST file.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-UpdateMessagePropertiesInPSTFile-.java" >}}
### **Updating Custom Properties for PST Items**
Sometimes it is required to mark items that are processed within the PST file. Aspose.Email API allows to achieve this using the [MapiProperty](https://apireference.aspose.com/java/email/com.aspose.email/mapiproperty) and [MapiNamedProperty](https://apireference.aspose.com/java/email/com.aspose.email/mapinamedproperty). The following methods are helpful in achieving this.

- MapiNamedProperty(long propertyTag, String nameIdentifier, UUID propertyGuid, byte[] propertyValue)
- MapiNamedProperty(long propertyTag, long nameIdentifier, UUID propertyGuid, byte[] propertyValue)
- FolderInfo.changeMessages(MapiPropertyCollection updatedProperties) - changes all messages in folder
- PersonalStorage.changeMessage(string entryId, MapiPropertyCollection updatedProperties) - change message properties



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-UpdateMessagePropertiesInPSTFile-UpdateCustomPropertiesInPst.java" >}}
## **Extract Attachments without Extracting Complete Message**
Aspose.Email API can be used to extract attachments from PST messages without extracting the complete message first. The [ExtractAttachments](https://apireference.aspose.com/java/email/com.aspose.email/PersonalStorage#extractAttachments\(com.aspose.email.MessageInfo\)) method of [PersonalStorage](https://apireference.aspose.com/java/email/com.aspose.email/personalstorage) class can be used to do this.
### **Extract Attachments from PST Messages**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-ExtractAttachments-.java" >}}
## **Adding Files to PST**
Microsoft Outlook's key functionality is managing emails, calendars, tasks, contacts and journal entries. In addition, files can also be added to a PST folder and the resulting PST keeps record of the documents added. Aspose.Email provides the facility to add files to a folder in the same way in addition to adding messages, contacts, tasks and journal entries to PST.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-AddFilesToPST-.java" >}}
## **String Searching in PST with Ignore Case**
Personal storage (PST) files can contain a huge amount of data and searching for data that meet specific criteria in such large files needs to include multiple checkpoints in the code to filter the information. This article shows how a PST can be searched based on a case sensitive string query.

To limit the number of results, it is possible to run a case sensitive search. This way, only words that match the string exactly, capitals and all, are returned. For a more general search, turn case sensitivity off and any words that contain the letters in the string, regardless of the casing, are returned.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-pst-StringSearchingInPSTWithIgnoreCase-.java" >}}
