---
title: Creating and Saving MSG files
type: docs
weight: 10
url: /java/creating-and-saving-msg-files/
---

{{% alert color="primary" %}} 

Aspose.Email can create Outlook message (MSG) files. The [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) class has a [save()](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage#save\(java.lang.String\)) method that can save the Outlook MSG file to disk or stream. The code snippet below creates an instance of the [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) class and set properties like from, to, subject, body, before saving it.

{{% /alert %}} 
### **Creating and Saving an MSG file**
To create and save an MSG file:

1. Creates a new instance of the [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) class and set properties such as from, to, subject and body.
1. Call the [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) class' [fromMailMessage()](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage#fromMailMessage\(com.aspose.email.MailMessage\)) method which accepts the object of the [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage).
1. Use the [fromMailMessage()](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage#fromMailMessage\(com.aspose.email.MailMessage\)) method to convert the [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) into [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) (MSG).
1. Calls the [MapiMessage.save()](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage#save\(java.lang.String\)) method to save the MSG file.

If you open the saved file in Microsoft Outlook, it will look like the screenshot below.

|![todo:image_alt_text](http://i.imgur.com/nx1w6WC.png)|
| :- |
|**Figure: The saved email message**|
The following code snippet shows the use of [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) and [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) classes to save the email in MSG file



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CreateAndSaveOutlookMessageFile-CreateAndSaveOutlookMessageFile.java" >}}
### **Save Message as Draft**
A draft is an unfinished message that has not yet been sent, instead, it is stored in a separate folder for future use. With Aspose.Email for Java, programmers can create a message using the [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) class and store it on disk using the [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) class.

Draft email messages are always in Outlook (MSG) format.

To save a draft email:

1. Create an instance of the [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) class.
1. Set the [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) object's properties like the subject, body, from, to and CC.
1. Create an instance of the [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) class.
1. Load a [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) instance in the [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) object using the [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) class' [fromMailMessage()](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage#fromMailMessage\(com.aspose.email.MailMessage\)) method.
1. Set the message flags using the [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) class' [setMessageFlags()](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessageItemBase#setMessageFlags\(long\)) method.
1. Save the message to disk in Outlook format using the [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) class' [save()](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage#save\(java.lang.String\)) method.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-email-SaveMessageAsDraft-.java" >}}
### **Implications of Body Compression**
The RTF body compression method can be used to generate a smaller size MSG. However, this results in slower speed. To creating messages with improved speed, set the flag to **false**. This flag, in turn, has an effect on the created PSTs: smaller MSG files result in smaller PST, and large MSG files result in slower PST creation.

**Smaller Size**

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CreateAndSaveOutlookMessageFile-BodyCompressionFlagSetToTrue.java" >}}



**Faster**

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CreateAndSaveOutlookMessageFile-BodyCompressionFlagSetToFalse.java" >}}
### **Preserving Original Email Address**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-email-ConvertEmailMessages-PreservingOriginalEmailAddress.java" >}}
### **Status of Recipients from a Meeting Request**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-email-ConvertEmailMessages-StatusOfRecipientsFromAMeetingRequest.java" >}}
### **Converting EML to MSG Preserving Embedded EML format**
EML files can be loaded into [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) class by instantiating a [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/mailmessage) object and passing it to [MapiMessage.FromMailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage#fromMailMessage\(com.aspose.email.MailMessage\)) method. If the EML file contains embedded EML files, use [MapiConversionOptions.setPreserveEmbeddedMessageFormat](https://apireference.aspose.com/java/email/com.aspose.email/MapiConversionOptions#setPreserveEmbeddedMessageFormat\(boolean\)) to retain the format of embedded EML files. The below code snippet shows how to load EML files into [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) while preserving the format of embedded EML files.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-email-PreservingEmbeddedMsgFormat-PreservingEmbeddedMsgFormat.java" >}}
