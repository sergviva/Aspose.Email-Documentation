---
title: Delete Messages
type: docs
weight: 20
url: /java/delete-messages/
---

[ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) can be used to delete messages from the server. Messages can be deleted using a message's sequence number of message id. The ImapClient's [deleteMessage](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#deleteMessage\(com.aspose.email.IConnection,%20int,%20long\)) is used to delete messages using any of these input parameters.
## **Delete Messages by Sequence Number**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-DeleteMessages-DeleteMessagesBySequenceNumber.java" >}}
## **Delete Messages using Message Id**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-DeleteMessages-DeleteMessagesUsingMessageId.java" >}}
## **Delete Set of Messages using Message UIDs**
In order to delete a set of messages using the messages' unique ids (UIDs), the API's [deleteMessagesByUids](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#deleteMessagesByUids\(com.aspose.email.IConnection,%20java.lang.Iterable\)) can be used as shown in the following code sample.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-DeleteMessages-DeleteSetOfMessagesUsingMessageUIDs.java" >}}
