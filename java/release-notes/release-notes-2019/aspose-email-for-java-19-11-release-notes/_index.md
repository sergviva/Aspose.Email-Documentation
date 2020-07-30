---
title: Aspose.Email for Java 19.11 Release Notes
type: docs
weight: 20
url: /java/aspose-email-for-java-19-11-release-notes/
---

{{% alert color="primary" %}} 

This page contains release notes information for Aspose.Email for Java 19.11.

{{% /alert %}} 
## **All Changes**


|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|EMAILNET-39614|Custom ordering of information in MHTML|Enhancement|
|EMAILNET-39629|PST password validation functionality not working|Enhancement|
|EMAILJAVA-34615|EML is not converted properly|Bug|
|EMAILNET-39626|IMAP exception on getting messages list if there are no emails in the server|Bug|
|EMAILNET-39632|Aspose.Email conversion Failure|Bug|
|EMAILNET-39633|Email Conversion Not working For Delivery Notifications|Bug|
|EMAILNET-39634|Recipient email is not getting changed using Aspose.Email|Bug|
|EMAILNET-39636|RTF body not showing in generated PDF|Bug|
|EMAILJAVA-34616|MapiCalendar Recurrence Exception without body|Bug|
|EMAILNET-39615|Set sender email address using MapiMessage in outlook|Bug|
|EMAILNET-39609|The email subject is read as a number|Bug|
|EMAILNET-39624|Envelop issue with EML file conversion|Bug|
|EMAILNET-39640|New line added on HtmlBodyText|Bug|
|EMAILNET-39656|Attachment missing on iOS mail app(iPhone/iPad)|Bug|
|EMAILJAVA-34619|MSG to PDF never ends|Bug|
|EMAILNET-39658|Aspose Email performance issue|Bug|
|EMAILNET-39630|The property PR_EMAIL_ADDRESS_W returns unexpected output|Bug|
|EMAILNET-39642|NullReferenceException while looping through storage.FolderHierarchy|Bug|
|EMAILJAVA-34624|Aspose license checks slow to perform  |Bug|

## **Custom ordering of information in MHTML**
**New property:** MhtSaveOptions.getRenderingHeaders
*Gets a list of headers for rendering. The order of headers rendering will correspond to the order of adding headers to the collection.*
### **Code samples**
- Renders headers in the order specified by default

{{< highlight csharp >}}

 String fileName = "test.eml";

MailMessage eml = MailMessage.load(fileName);

MhtSaveOptions opt = SaveOptions.getDefaultMhtml();

eml.save("test1.mhtml", opt);

{{< /highlight >}}

- Renders headers in the following order:
  - From
  - Subject
  - To
  - Sent

{{< highlight csharp >}}

 String fileName = "test.eml";

MailMessage eml = MailMessage.load(fileName);

MhtSaveOptions opt = SaveOptions.getDefaultMhtml();

opt.getRenderingHeaders().add(MhtTemplateName.FROM);

opt.getRenderingHeaders().add(MhtTemplateName.SUBJECT);

opt.getRenderingHeaders().add(MhtTemplateName.TO);

opt.getRenderingHeaders().add(MhtTemplateName.SENT);

eml.save("test2.mhtml", opt);

{{< /highlight >}}

- Renders headers in the following order:
  - Attachments
  - Cc
  - Subject

{{< highlight csharp >}}

 String fileName = "test.eml";

MailMessage eml = MailMessage.load(fileName);

MhtSaveOptions opt = SaveOptions.getDefaultMhtml();

opt.getRenderingHeaders().clear();

opt.getRenderingHeaders().add(MhtTemplateName.ATTACHMENTS);

opt.getRenderingHeaders().add(MhtTemplateName.CC);

opt.getRenderingHeaders().add(MhtTemplateName.SUBJECT);

eml.save("test3.mhtml", opt);

{{< /highlight >}}
## **PST password validation functionality**
**New property:** MessageStore.isPasswordProtected
*Gets a value indicating whether the storage is password protected.*

**New method:** MessageStore.isPasswordValid(String)
*Determines whether the specified string is a valid password for the storage.*
### **Code samples**
{{< highlight csharp >}}

 PersonalStorage pst = PersonalStorage.fromFile("NewPST.pst");

System.out.println("The storage is password protected - " + pst.getStore().isPasswordProtected());

{{< /highlight >}}

{{< highlight csharp >}}

 PersonalStorage pst = PersonalStorage.fromFile("NewPST.pst");

System.out.println("Password is valid - " + pst.getStore().isPasswordValid("test123"));

{{< /highlight >}}
## **Other**
New field MapiPropertyTag.PR_SMTP_ADDRESS
New field MapiPropertyTag.PR_SMTP_ADDRESS_W
