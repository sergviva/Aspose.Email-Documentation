---
title: Extracting Message Contents from Emails
type: docs
weight: 30
url: /net/extracting-message-contents-from-emails/
---

# Extracting Message Contents from Emails
## **Displaying Email Information on Screen**
The [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) represents an email message and allows developers to access email message properties. The header information (discussed in [Extracting Email Headers](#extracting-email-headers)) can be extracted and manipulated in different ways. This article explains how to display selected email header information and the email body on screen. To Display Email Information on Screen, follow these steps:

- Create an instance of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class.
- Load an email message into the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) instance.
- Display the email content on the screen.

The following code snippet shows you how to display email information on the screen.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-Email-DisplayEmailInformation-DisplayEmailInformation.cs" >}}
## **Extracting Email Headers**
The email header represents an Internet and RFC defined standard set of header fields included in Internet email messages. An email header can be specified using the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class. Common header types are defined in the [HeaderType](https://apireference.aspose.com/net/email/aspose.email/headertype) class. It is a sealed class working like normal enumeration. To extract headers from an email, follow these steps:

1. Create an instance of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class.
1. Load an email message in the instance of [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class.
1. After an email message has been loaded, we will get its raw content.

The [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class itself contains properties such as From, To, Cc, Subject and so on. These properties can be extracted from headers.

1. Display the raw content.

The following code snippet shows you how to extract email headers.


## **Get Decoded Header Values**
The following code snippet shows you how to get decoded header values.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-Email-GetDecodedHeaderValues-GetDecodedHeaderValue.cs" >}}
## **Get HTML body as plain text**
The [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class provides the feature to extract the HTML body of the message as plain text. The [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class provides a [GetHtmlBodyText](https://apireference.aspose.com/net/email/aspose.email/mailmessage/methods/gethtmlbodytext) method that returns the HTML body in plain text. The [GetHtmlBodyText](https://apireference.aspose.com/net/email/aspose.email/mailmessage/methods/gethtmlbodytext) method accepts a boolean parameter that indicates whether the body should contain URLs or not. Passing the parameter as true indicates that the HTML body should contain URLs.

The following code snippet demonstrates the use of [GetHtmlBodyText](https://apireference.aspose.com/net/email/aspose.email/mailmessage/methods/gethtmlbodytext) method to extract the HTML body of the email as plain text.



{{< gist "aspose-com-gists" "522d47278b8ca448dc1d7eb97193322c" "Examples-CSharp-Email-GetHTMLBodyAsPlainText-1.cs" >}}
