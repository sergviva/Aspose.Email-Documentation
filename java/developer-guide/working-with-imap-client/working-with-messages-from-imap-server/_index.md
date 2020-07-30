---
title: Working with Messages from IMAP Server
type: docs
weight: 80
url: /java/working-with-messages-from-imap-server/
---

## **Listing Messages with Paging Support**
With a large mailbox, comprising of hundreds of emails, it may not be suitable to list all the messages from the mailbox. Aspose.Email API provides support for listing messages from selected folder of the mailbox with paging support.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ListMessagesWithPagingSupport-.java" >}}
## **Listing Messages with MultiConnection**
[ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) provides a [UseMultiConnection](https://apireference.aspose.com/java/email/com.aspose.email/EmailClient#setUseMultiConnection\(int\)) property which can be used to create multiple connections for heavy operations. You may also set the number of connections to be used during multiconnection mode by using [ImapClient.ConnectionsQuantity](https://apireference.aspose.com/java/email/com.aspose.email/EmailClient#setConnectionsQuantity\(int\)). The following code snippet demonstrates the use of the multiconnection mode for listing messages and compares its performance with single connection mode.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ImapListMessagesWithMultiConnection-1.java" >}}

{{% alert color="primary" %}} 

Please note that the usage of multiconnection mode does not guarantee performance increase.

{{% /alert %}} 
## **Group Fetch Messages**
The [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class provides [fetchMessagesBySequences](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#fetchMessagesBySequences\(java.lang.Iterable\)) and [fetchMessagesByUids](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#fetchMessagesByUids\(java.lang.Iterable\)) methods which accepts iterable of Sequence Numbers or Unique ID and returns a list of [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage). The following code snippet demonstrates the use of the [fetchMessagesBySequences](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#fetchMessagesBySequences\(java.lang.Iterable\)) and [fetchMessagesByUids](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#fetchMessagesByUids\(java.lang.Iterable\)) methods to fetch messages by Sequence Numbers and Unique ID.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ImapFetchGroupMessages-1.java" >}}
## **Filtering Messages Based on Sender, Recipient or Date**
The [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class provides the [listMessages()](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#listMessages\(\)) method which gets all the messages from a mailbox. To get only messages which match some condition, use the overloaded [listMessages()](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#listMessages\(com.aspose.email.MailQuery\)) method which takes [MailQuery](https://apireference.aspose.com/java/email/com.aspose.email/MailQuery) as an argument. The [MailQuery](https://apireference.aspose.com/java/email/com.aspose.email/MailQuery) class provides various properties for specifying the conditions, for example, date, subject, sender, recipient and so on. This article shows how to filter email messages from a mailbox. The first example illustrates how to filter messages based on date and subject. We also show how to filter on other criteria and how to build more complex queries. The API also provides the capability to apply case-sensitive searching criteria to match exact filtering criteria. The API also allows specifying the search string encoding for filtering messages from the mailbox. The [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class provides the [listMessages()](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#listMessages\(\)) method which gets all the messages from a mailbox.
### **Filter Messages from Mailbox**
1. [Connect and log in to an IMAP server](/java/connecting-to-imap-server/)
1. Create an instance of the [MailQuery](https://apireference.aspose.com/java/email/com.aspose.email/MailQuery) and set the properties
1. Call the [ImapClient.ListMessages(MailQuery query)](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#listMessages\(com.aspose.email.MailQuery\)) method and pass the [MailQuery](https://apireference.aspose.com/java/email/com.aspose.email/MailQuery) with the parameters to get filtered messages only.

The following code snippet shows you how to connect to an IMAP mailbox and get messages that arrived today and have the word "newsletter" in the subject.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-FilterMessagesFromMailbox.java" >}}
### **Get Messages that Meet Specific Criteria**
The code samples above filter messages based on the email subject and date. We can use other properties to set other supported conditions as well. Below are some examples of setting the conditions using MailQuery.

The code snippets that follow show how to filter emails on:

1. Today's date
1. A date range
1. From a specific sender
1. From a specific domain
1. From a specific recipient
#### **Today's Date**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-FilterEmailBasedOnTodayDate.java" >}}
#### **Date Range**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-FilterEmailBasedOnDateRange.java" >}}
#### **Specific Sender**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-FilterEmailBasedOnSpecificSender.java" >}}
#### **Specific Domain**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-FilterEmailBasedOnSpecificDomain.java" >}}
#### **Specific Recipient**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-FilterEmailBasedOnSpecificRecepient.java" >}}
### **Filter and Display messages on Internal Date**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-FilterAndDisplayMessagesOnInternalDate.java" >}}
#### **Case Sensitive Email Filtering**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-CaseSensitiveEmailFiltering.java" >}}
#### **Specify Encoding for Query Builder**
The API's [ImapQueryBuilder](https://apireference.aspose.com/java/email/com.aspose.email/ImapQueryBuilder)'s constructor can be used to specify the Encoding for the search string. This can also be set using the DefaultEncoding property of the [MailQueryBuilder](https://apireference.aspose.com/java/email/com.aspose.email/MailQueryBuilder).

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-SpecifyEncodingForQueryBuilder.java" >}}
#### **Filter Messages and List with Paging Support**
In all the above code samples, we have shared how to filter messages using the [ImapQueryBuilder](https://apireference.aspose.com/java/email/com.aspose.email/ImapQueryBuilder). However, this may return a large number of emails and may take a long time if a large set of emails meet the criterion. Aspose.Email API provides the capability to search for messages from the mailbox while at the same time list the messages with paging support. The following code sample demonstrates the usage of this feature using the [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) API.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-FilterMessagesAndListWithPagingSupport.java" >}}
### **Filter Messages with Custom Flag**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FilterMessagesFromIMAPMailbox-GetMessageWithCustomFlag.java" >}}
## **Getting List-Unsubscribe Header Information**
List-Unsubscribe header contains the URL for unsubscribing from email lists e.g. advertisements, newsletters, etc. To get the List-Unsubscribe header, use the [ListUnsubscribe](https://apireference.aspose.com/java/email/com.aspose.email/MessageInfoBase#getListUnsubscribe\(\)) property of the [ImapMessageInfo](https://apireference.aspose.com/java/email/com.aspose.email/ImapMessageInfo) class. The following example shows the use of the [ListUnsubscribe](https://apireference.aspose.com/java/email/com.aspose.email/MessageInfoBase#getListUnsubscribe\(\)) property to get the List-Unsubscribe header.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-GetListUnsubscribeHeader-1.java" >}}
