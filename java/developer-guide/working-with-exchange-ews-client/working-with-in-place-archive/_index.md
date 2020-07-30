---
title: Working with In-Place Archive
type: docs
weight: 170
url: /java/working-with-in-place-archive/
---

## **In-Place Archives in Office 365**
In-Place Archives in Office 365 provides users with additional storage space. After the archive mailboxes are turned on, users can access and store messages in their Archive Mailbox by using Microsoft Outlook and Outlook on the Web. When the mailbox with In-Place archiving enabled is opened with Outlook, the archive mailbox is shown as a separate mailbox.
## **Move Items to In-Place Archive**
Aspose.Email API can be used to move items into users archive mailbox by using the [IEWSClient.archiveItem](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#archiveItem\(java.lang.String,%20java.lang.String\)) method. The [IEWSClient.archiveItem](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#archiveItem\(java.lang.String,%20java.lang.String\)) method provides four overloads which are listed below.

- [archiveItem(String sourceFolderUri, Appointment appointment)](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#archiveItem\(java.lang.String,%20com.aspose.email.Appointment\))
- [archiveItem(String sourceFolderUri, ExchangeTask task)](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#archiveItem\(java.lang.String,%20com.aspose.email.ExchangeTask\))
- [archiveItem(String sourceFolderUri, MapiMessageItemBase item)](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#archiveItem\(java.lang.String,%20com.aspose.email.MapiMessageItemBase\))
- [archiveItem(String sourceFolderUri, String uniqueId)](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#archiveItem\(java.lang.String,%20java.lang.String\))

The code example given below demonstrates the use of [IEWSClient.archiveItem](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#archiveItem\(java.lang.String,%20java.lang.String\)) method to move an email to the Archive Mailbox by using the UniqueUri.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchangeews-MoveItemsToInPlaceArchive-MoveItemsToInPlaceArchive.java" >}}
