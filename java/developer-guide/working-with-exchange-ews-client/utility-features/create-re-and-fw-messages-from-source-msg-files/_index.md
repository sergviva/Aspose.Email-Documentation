---
title: Create RE and FW messages from source MSG files
type: docs
weight: 30
url: /java/create-re-and-fw-messages-from-source-msg-files/
---

{{% alert color="primary" %}} 

IEWSClient lets developers create RE (reply/reply All) and FW (Forward) messages from a source message. The source message is identified by selecting a particular [ExchangeMessageInfo](https://apireference.aspose.com/java/email/com.aspose.email/exchangemessageinfo) from [ExchangeMessageInfoCollection](https://apireference.aspose.com/java/email/com.aspose.email/exchangemessageinfocollection) obtained by [IEWSClient.listMessages()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#listMessages\(\)). The other argument is the actual MailMessage to be sent as RE or FW message.

{{% /alert %}} 
## **Create RE/FW Message**
In the following example, a sample account is used to send a message and then the Reply and Forward message features are demonstrated against that sample message.

To perform this task:

1. Initialize the object by providing valid credentials.
1. Send a few sample messages.
1. Call the [IEWSClient.reply()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#reply\(com.aspose.email.MailMessage,%20com.aspose.email.ExchangeMessageInfo\)), [IEWSClient.replyAll()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#replyAll\(com.aspose.email.MailMessage,%20com.aspose.email.ExchangeMessageInfo\)) and [IEWSClient.forward()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#forward\(com.aspose.email.MailMessage,%20com.aspose.email.ExchangeMessageInfo\)) functions to send messages

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-CreateREAndFWMessage-.java" >}}
