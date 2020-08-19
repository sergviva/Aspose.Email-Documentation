---
title: Sending and Forwarding Messages
type: docs
weight: 20
url: /net/sending-and-forwarding-messages/
---


The [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class allows applications to send email using the Simple Mail Transfer Protocol (SMTP).

- The [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class is the only major entry developers use to send mail messages.
- The [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class also provides other common email delivery methods, including writing email messages to the file system, message queue etc.
- The [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class fully supports these two programming models:
  - [Synchronous](#sending-emails-synchronously)
  - [Asynchronous](#sending-emails-asynchronously)
- The [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class also supports [sending messages as TNEF](#sending-message-as-tnef)

To send the email message and block while waiting for the email to be transmitted to the SMTP server, use one of the synchronous Send methods. To allow your program's main thread to continue executing while the email is transmitted, use the [BeginSend](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/beginsend/index) method.
## **Sending Emails Synchronously**
An email message can be sent synchronously using the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class [Send](https://apireference.aspose.com/email/net/aspose.email.clients.smtp/smtpclient/methods/send/index) method. It sends the specified email message through an SMTP server for delivery. The message sender, recipients, subject, and message body are specified using String objects. To send an email message synchronously, follow the steps given below:

1. Create an instance of [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class and set its properties.
1. Create an instance of [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class and specify the Host, port, username & Password.
1. Send the Message using the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class [Send](https://apireference.aspose.com/net/email/aspose.email.clients.smtp.smtpclient/send/methods/5) method and pass the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) instance.

The following code snippet shows you how to send emails synchronously.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-SendEmailsSynchronously-SendEmailsSynchronously.cs" >}}
## **Sending Emails Asynchronously**
Sometimes, you may want to send mail asynchronously. For example, if you are sending a lot of mail through your application, the synchronous approach might not work. In such a scenario, you can use [BeginSend](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/beginsend/index). The [BeginSend](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/beginsend/index) method of the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class sends an email message to an SMTP server for delivery. This method does not block the calling thread and allows the caller to pass an object to the method that is invoked when the operation completes. To send an email message asynchronously, follow these steps:

1. Create an instance of [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class and use its different properties.
1. Create an instance of [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class and specify the host, port, username, and password.
1. Create a user-defined instance that will be passed to the method and invoked when the asynchronous operation completes.
1. Send the message using [BeginSend](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/beginsend/index) method of [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class and pass the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) instance and user-defined instance in it along with a callback function to be called when the operation is completed.

To receive a notification when the email has been sent or the operation has been canceled, the callback function passed to the [BeginSend](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/beginsend/index) method is called. After calling the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class [BeginSend](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/beginsend/index) method it is not necessary to wait for an email message to be sent completely. We can call another method [BeginSend](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/beginsend/index) at the same time. When an email has been sent using the [BeginSend](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/beginsend/index) method, the code snippet prints a message ("Message Sent"). The following code snippet shows you how to send emails asynchronously.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-SendEmailAsynchronously-SendEmailAsynchronously.cs" >}}
## **Sending Stored Messages from Disc**
EML files, (Outlook Express Electronic Mail files) contains an email's header, message body, and any attachments. Aspose.Email lets developers work with EML files in different ways. This article shows how to load EML files from disk and send them as emails with SMTP. You can load .eml files from disk or stream into the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class and send the email message using the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class. The [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class is the main class for creating new email messages, loading email message files from disk or stream and saving the messages. The following code snippet shows how to sending stored messages from the disc.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-LoadingEMLFilesFromDisk-LoadingEMLFilesFromDisk.cs" >}}
## **Sending Plain Text Email**
The programming samples below show how to send a plain text email message. The [Body](https://apireference.aspose.com/net/email/aspose.email/mailmessage/properties/body) property, a property of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class, is used to specify the plain text content of the message body. To send a plain text email message, follow these steps:

- Create an instance of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class.
- Specify the sender and receiver email addresses in the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) instance.
- Specify the [Body](https://apireference.aspose.com/net/email/aspose.email/mailmessage/properties/body) content, used for the plain text message.
- Create an instance of the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class and send the email.

The following code snippet shows you how to send a plain text email.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-SendPlainTextEmailMessage-SendPlainTextEmailMessage.cs" >}}
## **Sending Email with HTML body**
The programming samples below show how you can send a simple HTML email message. The [HtmlBody](https://apireference.aspose.com/net/email/aspose.email/mailmessage/properties/htmlbody), a property of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class, is used to specify the HTML content of the message body. To send a simple HTML email, follow these steps:

- Create an instance of the [MailMessage](http://www.aspose.com/api/net/email/aspose.email.mail/mailmessage) class.
- Specify sender and receiver email address in the [MailMessage](http://www.aspose.com/api/net/email/aspose.email.mail/mailmessage) instance.
- Specify the [HtmlBody](https://apireference.aspose.com/net/email/aspose.email/mailmessage/properties/htmlbody) content.
- Create an instance of the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class and send the email using the [Send](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/send/index) method.

For the purposes of this article, the HTML content of the email is rudimentary: <html><body>This is the HTML body</body></html> Most HTML emails will be more complex. The following code snippet shows you how to send an email with HTML body.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-SettingHTMLBody-SettingHTMLBody.cs" >}}
## **Sending Email with Alternate Message Text**
The programming samples below show how to send a simple HTML email message with alternative content. Use the [AlternateView](https://apireference.aspose.com/net/email/aspose.email/alternateview) class to specify copies of an email message in different formats. For example, if you send a message in HTML, you might also want to provide a plain text version for recipients who use email readers that cannot display HTML content. Or, if you are sending a newsletter, you might want to provide a plain text copy of the text for those recipients who have chosen to receive a plain text version. To send an email with alternate text, follow these steps:

1. Create an instance of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class.
1. Specify sender and receiver email addresses in the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) instance.
1. Create an instance of the [AlternateView](https://apireference.aspose.com/net/email/aspose.email/alternateview) class.

This creates an alternate view to an email message using the content specified in the string.

1. Add the instance of the [AlternateView](https://apireference.aspose.com/net/email/aspose.email/alternateview) class to the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) object.
1. Create an instance of the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class and send the email using the [Send](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/send/index) method.

The following code snippet shows you how to send an email with alternate text.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-Email-SetAlternateText-SetAlternateText.cs" >}}
## **Sending Bulk Emails**
Sending emails in bulk means sending a batch of emails in one message. We can send a batch of email using the of [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class [Send](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/send/index) method overload that accepts a [MailMessageCollection](https://apireference.aspose.com/net/email/aspose.email/mailmessagecollection):

1. Create an instance of [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class.
1. Specify the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class properties.
1. Create an instance of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class.
1. Specify sender, receiver, mail subject and message in the instance of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class.
1. Repeat the above two steps again, if you want to send email to a different person.
1. Create an instance of [MailMessageCollection](https://apireference.aspose.com/net/email/aspose.email/mailmessagecollection) class.
1. Add an instance of [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class in the object of the [MailMessageCollection](https://apireference.aspose.com/net/email/aspose.email/mailmessagecollection) class.
1. Now send your email using the [SmtpClient](http://www.aspose.com/api/net/email/aspose.email.mail/smtpclient) class [Send](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/send/index) method by passing the instance of [MailMessageCollection](http://www.aspose.com/api/net/email/aspose.email.mail/mailmessagecollection) class in it.

The following code snippet shows you how to send bulk emails.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-SendingBulkEmails-SendingBulkEmails.cs" >}}
## **Sending Emails with MultiConnection**
[SmtpClient](http://www.aspose.com/api/net/email/aspose.email.mail/smtpclient) provides a [UseMultiConnection](https://apireference.aspose.com/net/email/aspose.email.clients/emailclient/properties/usemulticonnection) property which can be used to create multiple connections for heavy operations. You may also set the number of connections to be used during multiconnection mode by using [SmtpClient.ConnectionsQuantity](https://apireference.aspose.com/net/email/aspose.email.clients/emailclient/properties/connectionsquantity). The following code snippet demonstrates the use of the multiconnection mode for sending multiple messages.



{{< gist "aspose-com-gists" "522d47278b8ca448dc1d7eb97193322c" "Examples-CSharp-SMTP-SendWithMultiConnection-1.cs" >}}

{{% alert color="primary" %}} 

Please note that the usage of multiconnection mode does not guarantee performance increase.

{{% /alert %}} 
## **Sending Message as TNEF**
TNEF emails have special formatting which may be lost if sent using the standard API. Aspose.Email provides the capability to send emails as TNEF, thus preserving the format. The [SmtpClient](http://www.aspose.com/api/net/email/aspose.email.mail/smtpclient) class [UseTnef](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/properties/usetnef) property can be set to send the email as TNEF. The following code snippet shows you how to send a message as TNEF.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-SendMessageAsTNEF-SendMessageAsTNEF.cs" >}}
## **Sending Meeting Requests**
Microsoft Outlook offers calendar functions as well as email management. When a user opens an email with an invitation to an event, Outlook prompts them to accept or reject the invitation. Aspose.Email lets developers add calendar functions to your emails.
### **Sending Requests via Email**
To send meeting requests via email, follow these steps:

- Create an instance of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class.
- Specify sender and recipient addresses using an instance of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class.
- Initialize an instance of the [Appointment](https://apireference.aspose.com/net/email/aspose.email.calendar/appointment) class and pass its values.
- Specify summary and description in the [Calendar](https://apireference.aspose.com/net/tasks/aspose.tasks/calendar) instance.
- Add the [Calendar](https://apireference.aspose.com/net/tasks/aspose.tasks/calendar) to the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) instance and pass it the [Appointment](https://apireference.aspose.com/net/email/aspose.email.calendar/appointment) instance.

|**iCalendar meeting request sent by email**|
| :- |
|![todo:image_alt_text](sending-and-forwarding-messages_1.png)|
The following code snippet shows you how to send requests via Email.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-MeetingRequests-SendingMeetingRequestsViaEmail.cs" >}}
### **iCalendar supports for IBM Lotus Notes**
Aspose.Email calendar feature is based on the iCalendar standard, a standard for calendar data exchange (RFC 2445 or RFC2445 Syntax Reference). Therefore, it supports not only Microsoft Outlook but also IBM Lotus Notes. To send a meeting request in Lotus Notes, follow the same steps as mentioned above.
## **Forward an Email using SMTP Client**
### **Forwarding Email with SMTP client**
Forwarding an email is common practice in daily life digital communication. An email received can be forwarded to specific recipients without sharing with the original senders. Aspose.Email API's [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) provides the capability to forward an email to specific recipients. Its Forward method can be used to forward a received or saved email to desired recipients as shown in this article. The following code snippet shows you how to Forward an Email using SMTP Client.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-ForwardEmail-ForwardEmail.cs" >}}
### **Forwarding Email without using MailMessage**
The API also supports forwarding EML messages without first loading into [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage). This is useful in cases where there are limited resources in terms of system memory.

{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-ForwardEmailWithoutUsingMailMessage-ForwardEmailWithoutUsingMailMessage.cs" >}}
## **Performing Mail Merge**
Mail merges help you create and send a batch of similar email messages. The core of the emails are the same, but the content can be personalized. Typically, a recipient's contact details (first name, second name, company and so on) are used to personalize the email.

|**Illustration of how a mail merge works:**|
| :- |
|![todo:image_alt_text](sending-and-forwarding-messages_2.png)|
Aspose.Email lets developers set up mail merges that include data from a variety of data sources.

To perform a mail merge with Aspose.Email, take the following steps:

1. Create a function with the name signature
1. Create an instance of the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) class.
1. Specify the sender, receiver, subject, and body.
1. Create a signature for the end of the email.
1. Create an instance of the [TemplateEngine](https://apireference.aspose.com/net/email/aspose.email.tools.merging/templateengine) class and pass it the [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) instance.
1. Take signature in the [TemplateEngine](https://apireference.aspose.com/net/email/aspose.email.tools.merging/templateengine) instance.
1. Create an instance of the DataTable class.
1. Add the columns **Receipt**, **FirstName** and **LastName** as data sources in the DataTable class.
1. Create an instance of the DataRow class.
1. Specify the receipt address, first and last names in the DataRow object.
1. Create an instance of the [MailMessageCollection](https://apireference.aspose.com/net/email/aspose.email/mailmessagecollection) class
1. Specify the [TemplateEngine](https://apireference.aspose.com/net/email/aspose.email.tools.merging/templateengine)  and DataTable instances in the [MailMessageCollection](https://apireference.aspose.com/net/email/aspose.email/mailmessagecollection) instance.
1. Create an instance of the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class and specify the server, port, username, and password.
1. Send emails using the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class [Send](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient/methods/send/index) method.

In the sample below, #FirstName# indicates a column's DataTable, whose value is set by the user. The following code snippet shows you how to perform Mail Merge.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-MailMerge-MailMerge.cs" >}}
## **Performing Row-Wise Mail Merge**
User can merge individual data row as well to get a complete and prepared [MailMessage](https://apireference.aspose.com/net/email/aspose.email/mailmessage) object. The [TemplateEngine.Merge](https://apireference.aspose.com/net/email/aspose.email.tools.merging/templateengine/methods/merge/index) method can be used to perform a row-wise mail merge.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-RowWiseMailMerge-RowWiseMailMerge.cs" >}}
