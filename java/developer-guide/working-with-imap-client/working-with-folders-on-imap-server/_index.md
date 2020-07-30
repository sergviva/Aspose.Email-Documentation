---
title: Working with Folders on IMAP Server
type: docs
weight: 50
url: /java/working-with-folders-on-imap-server/
---

## **Getting Folders Information**
Getting information about folders from an IMAP server is very easy with Aspose.Email. The [listFolders()](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#listFolders\(\)) method of [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) returns an object of the [ImapFolderInfoCollection](https://apireference.aspose.com/java/email/com.aspose.email/ImapFolderInfoCollection) that contains information about all the server folders. Iterate through this collection and get information about individual folders in a loop. The method is overloaded. You can pass a folder name as a parameter to get a list of subfolders.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-GetFoldersInformation-.java" >}}
## **Adding a New Message in a Folder**
Aspose.Email's [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) allows adding a new message to a folder. [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage) can be used to create a new message and append it to a server's folder.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-AddANewMessageToAFolder-.java" >}}
## **Add Multiple Messages with MultiConnection Support**
You can add multiple messages by using the [AppendMessages](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#appendMessages\(com.aspose.email.IConnection,%20java.lang.Iterable\)) method provided by the [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) classes. The [AppendMessages](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#appendMessages\(com.aspose.email.IConnection,%20java.lang.Iterable\)) method accepts a list of [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage) and adds it to the current folder if the folder is not provided as a parameter. ImapClient also supports MultiConnection mode for heavy loaded operations. The following code snippet shows you how to add multiple messages by using the MultiConnection mode.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ImapGroupAppendWithMultiConnection-1.java" >}}

{{% alert color="primary" %}} 

Please note that the usage of multiconnection mode does not guarantee performance increase.

{{% /alert %}} 
## **Move Messages to Another Mailbox Folder**
Aspose.Email API provides the capability to move a message from one folder of a mailbox to another. The ImapClient's [moveMessage](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#moveMessage\(com.aspose.email.IConnection,%20java.lang.String,%20java.lang.String\)) method and it's overloads provides the facility to move a message using its unique id or sequence number to another folder.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-MoveMessagesFromOneFolderToAnother-.java" >}}
## **Copy Message to Another Mailbox Folder**
Aspose.Email API provides the capability to copy message from one mailbox folder to another. It allows copying a single as well as multiple messages using the [copyMessage](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#copyMessage\(int,%20java.lang.String\)) and [copyMessages](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#copyMessages\(com.aspose.email.IConnection,%20int,%20int,%20java.lang.String\)) methods. The [copyMessages](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#copyMessages\(com.aspose.email.IConnection,%20int,%20int,%20java.lang.String\)) method provides the capability to copy multiple messages from source folder of a mailbox to the destination mailbox folder. The following code sample illustrates this by copying two messages.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-CopyMessagesFromOneFolderToAnother-.java" >}}
## **Working with Special-Use Mailbox Folders**
Some IMAP message stores include special-use mailboxes, such as those used to hold draft messages or sent messages. Many mail clients allow users to specify where the draft or sent messages should be put, but configuring them requires that the user know which mailboxes the server has set aside for these purposes. Aspose.Email can identify these special-use mailboxes by using the [ImapMailboxInfo](https://apireference.aspose.com/java/email/com.aspose.email/ImapMailboxInfo) class to make it easier to work with them. The following code sample demonstrates how to access these special-use mailboxes by using the [ImapMailboxInfo](https://apireference.aspose.com/java/email/com.aspose.email/ImapMailboxInfo) class.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ImapSpecialUseMailboxes-1.java" >}}
