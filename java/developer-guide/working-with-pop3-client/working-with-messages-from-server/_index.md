---
title: Working with Messages from Server
type: docs
weight: 30
url: /java/working-with-messages-from-server/
---

## **Getting Mailbox Information**
We can get information about the mailbox such as the number of messages and the mailbox size using the [getMailBoxSize()](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client#getMailboxSize\(\)) and [getMailBoxInfo()](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client#getMailboxInfo\(\)) methods of the [Pop3Client](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client) class.

- The [getMailBoxSize()](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client#getMailboxSize\(\)) method returns the size of the mailbox in bytes.
- The [getMailBoxInfo()](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client#getMailboxInfo\(\)) method returns an object of type [Pop3MailBoxInfo](https://apireference.aspose.com/java/email/com.aspose.email/Pop3MailboxInfo).

It is also possible to get the number of messages using the [getMessageCount()](https://apireference.aspose.com/java/email/com.aspose.email/Pop3MailboxInfo#getMessageCount\(\)) method and the size using the [getOccupiedSize()](https://apireference.aspose.com/java/email/com.aspose.email/Pop3MailboxInfo#getOccupiedSize\(\)) method of the [Pop3MailBoxInfo](https://apireference.aspose.com/java/email/com.aspose.email/Pop3MailboxInfo) class.

The following code demonstrates how to retrieve Mailbox information and get the message count and occupied size using the Aspose.Email API.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-pop3-GetMailboxInformation-.java" >}}
## **Retrieving Email Headers**
Email headers can give us information about an email message that we can use to decide whether or not to retrieve the whole email message. Typically, the header information contains sender, subject, received date, etc. Aspose.Email's POP3 client can be used to retrieve message headers from a server based on the protocol's specifications.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-pop3-RetrieveEmailHeaders-.java" >}}
## **Listing Messages with MultiConnection**
[Pop3Client](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client) provides a [UseMultiConnection](https://apireference.aspose.com/java/email/com.aspose.email/EmailClient#setUseMultiConnection\(int\)) property which can be used to create multiple connections for heavy operations. You may also set the number of connections to be used during multiconnection mode by using [Pop3Client.ConnectionsQuantity](https://apireference.aspose.com/java/email/com.aspose.email/EmailClient#setConnectionsQuantity\(int\)). The following code snippet demonstrates the use of the multiconnection mode for listing messages and compares its performance with single connection mode.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-pop3-Pop3ListMessagesWithMultiConnection-1.java" >}}

{{% alert color="primary" %}} 

Please note that the usage of multiconnection mode does not guarantee performance increase.

{{% /alert %}} 
## **Retrieving Email Messages and Saving**
Aspose.Email's [Pop3Client](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client) provides the capability to retrieve email messages from the POP3 server, and parse them into a [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage) instance with the help of Mail components. The [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage) class contains several properties and methods for manipulating email content. By using the [Pop3Client](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client) class' [FetchMessage](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client#fetchMessage\(int\)) function, you can get a MailMessage instance directly from the POP3 server.
### **Retrieve Messages using Sequence Number**
Message sequence numbers start from 1 for the messages in the mailbox. Pop3Client of Aspose.Email allows retrieving messages using the sequence number. Retrieved messages can be saved to disc as well as to stream. Since the message is retrieved in an instance of [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage), it can be saved in any format such as EML, MSG or MHTML. The following code sample demonstrates how to achieve this using Aspose.Email for Java.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-pop3-RetrieveEmailMessages-RetrieveMessagesUsingSequenceNumber.java" >}}
### **Retrieve Messages using Message Unique URI**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-pop3-RetrieveEmailMessages-RetrieveMessagesUsingMessageUniqueURI.java" >}}
### **Retrieve and Save directly to disc**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-pop3-RetrieveEmailMessages-RetrieveAndSaveDirectlyToDisc.java" >}}
## **Getting Message Summary Information**
Aspose.Email API's [Pop3Client](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client) lets you retrieve message summary information that is represented by the [Pop3MessageInfo](https://apireference.aspose.com/java/email/com.aspose.email/Pop3MessageInfo) class. The [ListMessages](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client#listMessages\(\)) method of the client returns a collection of the [Pop3MessageInfo](https://apireference.aspose.com/java/email/com.aspose.email/Pop3MessageInfo) entries that can further be used to fetch a message or build meta-information storage systems. Message summary information can be retrieved using:

- Message's Sequence Number
- Message's Unique Id
### **Retrieve Message Summary Information using Sequence Number**


{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-pop3-GetMessageSummaryInformation-RetrieveMessageSummaryInformationUsingSequenceNumber.java" >}}
### **Retrieve Message Summary Information using Unique Id**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-pop3-GetMessageSummaryInformation-RetrieveMessageSummaryInformationUsingUniqueId.java" >}}
## **Group Fetch Messages**
[Pop3Client](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client) provides [fetchMessagesBySequences](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client#fetchMessagesBySequences\(java.lang.Iterable\)) and [fetchMessagesByUids](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client#fetchMessagesByUids\(java.lang.Iterable\)) methods which accepts iterable of Sequence Numbers or Unique ID and returns a list of [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage). The following code snippet demonstrates the use of [fetchMessagesBySequences](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client#fetchMessagesBySequences\(java.lang.Iterable\)) and [fetchMessagesByUids](https://apireference.aspose.com/java/email/com.aspose.email/Pop3Client#fetchMessagesByUids\(java.lang.Iterable\)) methods to fetch messages by Sequence Numbers and Unique ID.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-pop3-Pop3FetchGroupMessages-1.java" >}}
