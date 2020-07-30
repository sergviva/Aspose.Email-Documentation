---
title: Managing Message Files with Aspose.Email.Outlook
type: docs
weight: 20
url: /java/managing-message-files-with-aspose-email-outlook/
---

## **Converting MSG to MIME message**
Aspose.Email API provides the capability of converting MSG files to MIME messages using the [toMailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage#toMailMessage\(com.aspose.email.MailConversionOptions\)) method.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CreateAndSaveOutlookMessageFile-ConvertMSGToMIMEMessage.java" >}}
## **Read and Write Outlook Template File (OFT)**
Outlook templates are very useful when you want to send a similar email message again and again. Instead of preparing the message from scratch each time, you can first prepare the message in Microsoft Outlook and save it as an Outlook Template (OFT). After that, if you need to send the message, create it from the template and save time for writing up the same text in the body, subject, etc.

Aspose.Email's [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) class can be used to load a Microsoft Outlook template (OFT) file. Once the Outlook template is loaded in an instance of the [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) class, you may update the sender, recipient, body, subject and other properties. After updating the properties, you can

- send the email using [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient) class, or
- save the message as MSG and do further updates or validation using Microsoft Outlook.

In the below screenshot, you can see a meeting invitation template, which is prepared using Microsoft Outlook and saved as an Outlook template (OFT). The example code loads this template using the [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) class, updates some of the properties and saves the message in MSG format.

|![todo:image_alt_text](http://i.imgur.com/R2XRpyP.png)|
| :- |
|**Figure: Email template**|
After running the code, the email will look like the message below when it is opened in Microsoft Outlook.

|![todo:image_alt_text](http://i.imgur.com/QDxblVc.png)|
| :- |
|**Figure: The output email**|
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-ReadAndWriteOutlookTemplateFile-ReadAndWriteOutlookTemplateFile.java" >}}
### **Save as Outlook Template File (OFT)**
Just as the API can read OFT files, it also provides the capability to write to OFT files as shown in the following code sample.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-ReadAndWriteOutlookTemplateFile-SaveAsOutlookTemplateFile.java" >}}
## **Setting Color Category for Outlook Message (MSG) Files**
Microsoft Outlook lets users assign color categories to differentiate emails. A color category marks an email as being of some kind of importance or category. Aspose.Email provides the same feature through the [FollowUpManager](https://apireference.aspose.com/java/email/com.aspose.email/FollowUpManager) class. The following functionality is supported via this class:

- [addCategory()](https://apireference.aspose.com/java/email/com.aspose.email/FollowUpManager#addCategory\(com.aspose.email.MapiMessage,%20java.lang.String\)) takes [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage) and the color category string as arguments.
- [removeCategory()](https://apireference.aspose.com/java/email/com.aspose.email/FollowUpManager#removeCategory\(com.aspose.email.MapiMessage,%20java.lang.String\)) takes [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage) and the color category string to be removed from the message as arguments.
- [clearCategories()](https://apireference.aspose.com/java/email/com.aspose.email/FollowUpManager#clearCategories\(com.aspose.email.MapiMessage\)) is used to remove all the color categories from the message.
- [getCategories()](https://apireference.aspose.com/java/email/com.aspose.email/FollowUpManager#getCategories\(com.aspose.email.MapiMessage\)) is used to retrieve all the color categories from a particular message.

The following example performs the tasks as given below:

1. Add a color category.
1. Add another color category.
1. Retrieve the list of all categories.
1. Remove all categories.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-SetColorCategoryForOutlookMessageFile-.java" >}}
## **Accessing Follow Up Information from Message**
Aspose.Email API provides the capability to access the follow-up information from a sent or received message. It can retrieve the Read, Delivery Read Receipt and vote results information from a message file.
### **Retrieve Read and Delivery Receipt Information**


{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-AccessFollowUpInformationFromMessage-RetrievingReadAndDeliveryReceiptInformation.java" >}}
### **Read the Vote Results Information**


{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-AccessFollowUpInformationFromMessage-ReadTheVoteResultsInformation.java" >}}
## **Creating Forward and Reply Messages**
Aspose.Email API provides the capability of creating and formatting the forward and reply messages. The [ReplyMessageBuilder](https://apireference.aspose.com/java/email/com.aspose.email/ReplyMessageBuilder) and [ForwardMessageBuilder](https://apireference.aspose.com/java/email/com.aspose.email/ForwardMessageBuilder) classes of the API are used to create the Reply and Forward messages respectively. A Reply or Forward message can be specified to be created using any of the modes of [OriginalMessageAdditionMode](https://apireference.aspose.com/java/email/com.aspose.email/OriginalMessageAdditionMode) enum. This enum has the following values:

- [OriginalMessageAdditionMode.None](https://apireference.aspose.com/java/email/com.aspose.email/OriginalMessageAdditionMode#None) - The original message is not included in the response message.
- [OriginalMessageAdditionMode.Attachment](https://apireference.aspose.com/java/email/com.aspose.email/OriginalMessageAdditionMode#Attachment) - The original message is included as an attachment in the response message
- [OriginalMessageAdditionMode.Textpart](https://apireference.aspose.com/java/email/com.aspose.email/OriginalMessageAdditionMode#Textpart) - The original message is included as text in the body of the response message
### **Create Reply Message**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CreateForwardAndReplyMessage-CreateReplyMessage.java" >}}
### **Create Forward Message**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CreateForwardAndReplyMessage-CreateForwardMessage.java" >}}
