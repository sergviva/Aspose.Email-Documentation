---
title: Fetch Messages from an Exchange Server Mailbox
type: docs
weight: 30
url: /java/fetch-messages-from-an-exchange-server-mailbox/
---

{{% alert color="primary" %}} 

Listing Messages on an Exchange Server used the [listMessages()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#listMessages\(\)) method to get a list of messages from an Exchange Server mailbox. The [listMessages()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#listMessages\(\)) method gets basic information about messages, for example, the subject, the message ID, from and to.

To get the complete message details, Aspose.Email.Exchange provides the [fetchMessage()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#fetchMessage\(java.lang.String\)) method. This method accepts the message URI as a parameter and returns an instance of the [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage) class. The [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage) class then provides message details like the body, headers, and attachments.

{{% /alert %}} 
## **Fetch Messages from an Exchange Server Mailbox**
Similarly, you can get message details from any folder by passing the correct folder URI to the [listMessages()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#listMessages\(\)) method. To fetch messages from the Inbox folder using Exchange Web Services, you need to use the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) class provided in the *com.aspose.email* namespace. This method uses Exchange Web Services (EWS) to connect and retrieve messages from the Exchange Server.
The following code snippet demonstrates fetching messages using EWS:

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-FetchMessagesFromAnExchangeServerMailbox-FetchMessagesFromAnExchangeServerMailboxUsingEWS.java" >}}



