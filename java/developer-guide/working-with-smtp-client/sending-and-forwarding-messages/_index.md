---
title: Sending and Forwarding Messages
type: docs
weight: 20
url: /java/sending-and-forwarding-messages/
---

## **Sending Emails**
The [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient) class provided by Aspose.Email for Java API allows sending email using the Simple Mail Transfer Protocol (SMTP).

- The [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient) class is the only major entry developers use to send mail messages.
- The [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient) class also provides other common email delivery methods, including writing email messages to the file system, message queue, etc.
- The [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient) class also supports sending messages as TNEF.
- It allows sending emails via non-SSL as well as SSL enabled servers.

This article shows how to use the SmtpClient class to send email messages.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-smtp-SendEmails-.java" >}}
## **Sending Meeting Request**
Aspose.Email for Java API already allows working with Appointments/meetings such as creating an appointment, formatting and saving it to disc and add as well as retrieve attachments from these. With the API's [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient), these meeting requests can be sent out to the recipients similar to Microsoft Outlook. This article shows how to send a meeting request using the API's [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient).

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-smtp-SendMeetingRequest-.java" >}}
## **Sending Emails with MultiConnection**
[SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient) provides a [UseMultiConnection](https://apireference.aspose.com/java/email/com.aspose.email/EmailClient#setUseMultiConnection\(int\)) property which can be used to create multiple connections for heavy operations. You may also set the number of connections to be used during multiconnection mode by using [SmtpClient.ConnectionsQuantity](https://apireference.aspose.com/java/email/com.aspose.email/EmailClient#setConnectionsQuantity\(int\)). The following code snippet demonstrates the use of the multiconnection mode for sending multiple messages.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-smtp-SendWithMultiConnection-1.java" >}}

{{% alert color="primary" %}} 

Please note that the usage of multiconnection mode does not guarantee performance increase.

{{% /alert %}} 
## **Forwarding Emails using SMTP Client**
### **Forwarding Email**
Forwarding an email is common practice in daily life digital communication. An email received can be forwarded to specific recipients without sharing with the original senders. Aspose.Email API's [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient) provides the capability to forward an email to specific recipients. Its [forward](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient#forward\(com.aspose.email.IConnection,%20java.lang.String,%20java.lang.String,%20com.aspose.email.MailMessage\)) method can be used to forward a received or saved email to desired recipients as shown in this article.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-smtp-ForwardAnEmailUsingSMTPClient-.java" >}}
### **Forwarding Email Without Loading using MailMessage**
In certain cases, a system may be low on resources like Memory. Using [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage), in such scenarios, can lead to problems before sending via Smtp client. The API provides the capability to send email messages without loading it using [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage) instance. Following sample code illustrates the usage of this feature.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-smtp-ForwardEmailWithoutUsingMailMessage-ForwardEmailWithoutMailMessage.java" >}}
