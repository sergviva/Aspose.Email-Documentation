---
title: Get MailTips from Exchange Server
type: docs
weight: 50
url: /java/get-mailtips-from-exchange-server/
---

{{% alert color="primary" %}} 

Microsoft Exchange Server added several new features with Exchange Server 2010 and 2013. One of them lets users get mail tips when composing an email message. These tips are very useful as they provide information before the email is sent. For example, if an email address is wrong in the recipient’s list, a tip is displayed to let you know that the email address is invalid.

Mail tips also let you see out of office replies before sending an email: Exchange Server (2010 & 2013) sends the mail tip when the email is being composed if one or more of the recipients have set out of office replies.

{{% /alert %}} {{% alert color="primary" %}} 

Microsoft Exchange Server 2010 Service Pack 1 is required for all the features demonstrated in this article.

{{% /alert %}} 
## **Get Mail Tips**
The below example uses the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class which uses Exchange Web Services, available in Microsoft Exchange Server 2007 and later versions.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-GetMailTipsFromExchangeServer-.java" >}}
