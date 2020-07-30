---
title: IMAP Backup and Restore Operation
type: docs
weight: 90
url: /java/imap-backup-and-restore-operation/
---

Aspose.Email for .NET provides the ability to backup and restore messages. For this, the API provides the following methods.

- [ImapClient.Backup](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#backup\(com.aspose.email.ImapFolderInfoCollection,%20java.lang.String,%20com.aspose.email.BackupSettings\))
- [ImapClient.Restore](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient/methods/restore/index)

This article demonstrates how to backup and restore messages using the [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class.
## **Backup Messages**
To backup messages, use the [ImapClient.Backup](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#backup\(com.aspose.email.ImapFolderInfoCollection,%20java.lang.String,%20com.aspose.email.BackupSettings\)) method as demonstrated in the following code snippet.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ImapBackupOperation-1.java" >}}
## **Restore Messages**
To backup messages, use the [ImapClient.Restore](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#restore\(com.aspose.email.PersonalStorage,%20com.aspose.email.ImapRestoreSettings\)) method as demonstrated in the following code snippet.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ImapRestoreOperation-1.java" >}}
## **IMAP Backup and Restore Operation with MultiConnection**
When working with a large number of messages, the backup/restore operation can take a long time. For this, the API provides support for multiple connections during backup and restore operation. To enable the MultiConnection mode, set [ImapClient.UseMultiConnection](https://apireference.aspose.com/java/email/com.aspose.email/EmailClient#setUseDefaultCredentials\(boolean\)) property to [MultiConnectionMode.Enable](https://apireference.aspose.com/java/email/com.aspose.email/MultiConnectionMode#Enable). The following code snippets demonstrate backup and restore operation with MultiConnection mode enabled.
### **Backup Messages with MultiConnection**
The following code snippets demonstrate backup operation with MultiConnection mode enabled.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ImapBackupOperationWithMultiConnection-1.java" >}}
### **Restore Messages with MultiConnection**
The following code snippets demonstrate restore operation with MultiConnection mode enabled.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ImapRestoreOperationWithMultiConnection-1.java" >}}
