---
title: Aspose.Email for Android via Java 20.7 Release Notes
type: docs
weight: 9
url: /androidjava/aspose-email-for-android-via-java-20-7-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes information for Aspose.Email for Android via Java 20.7 

{{% /alert %}}
## **All Changes**


|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|EMAILNET-39844|Message to HTML - how to preserve embedded attachment's icons and text|Feature|
|EMAILNET-39852|Support for getting Email Category in MHTML|Feature|
|EMAILNET-39876|Support for countering endless wait or zombie condiation for Aspose.Email operations|Feature|
|EMAILNET-39794|Set Timezone is not visible in MS Outlook 2016|Enhancement|
|EMAILJAVA-34701|Multipart/related part marked with content-dispotion attachment missing in MailMessage|Enhancement|
|EMAILJAVA-34700|Text wrapping getting disturbed in case of lengthy CC/TO fields in exported PDF|Enhancement|
|EMAILNET-39835|Add overload for SaveAs with Stream input in PersonalStorage|Enhancement|
|EMAILNET-39834|Add overload for MergeWith with Streams in PersonalStorage|Enhancement|
|EMAILNET-39860|MapiCalendar does not have public property for organizer|Enhancement|
|EMAILNET-39858|No messages are read from MBOX|Enhancement|
|EMAILNET-39843|Text wrapping getting disturbed in case of lengthy CC/TO fields in exported PDF|Enhancement|
|EMAILJAVA-34726|Provision to make IDisposible extend Closeable|Enhancement|
|EMAILNET-39823|Can't save MailMessage with default Date|Bug|
|EMAILNET-39705|Meeting opened as appointment in saved PST when viewed in MS Outlook|Bug|
|EMAILNET-39803|Office 365 Recurrence ICS not getting Appended|Bug|
|EMAILNET-39811|Extra symbols are in the message body|Bug|
|EMAILJAVA-34691|Memory issue loading MapiMessage|Bug|
|EMAILNET-39818|MSG to MHTML wrong sent time extracted|Bug|
|EMAILNET-39820|Aspose.Email: there are unclosed tags in the HtmlBody after loading an .msg file|Bug|
|EMAILJAVA-34697|Erroneous meeting end times on recurring meetings|Bug|
|EMAILNET-39816|Parsing Appointment resulting recurrency error rule error|Bug|
|EMAILNET-39839|Table borders disappeared while converting msg|Bug|
|EMAILNET-39871|Embedded images appearing in attachments of save MSG|Bug|
|EMAILNET-39853|Attachments lost during Appointment to MapiCalendar conversion|Bug|
|EMAILNET-39856|EML Content are not read properly|Bug|
|EMAILNET-39865|NullReferenceException on extracting messages form PST|Bug|
|EMAILNET-39854|Incorrect PropertyDescriptor's for the named properties in MapiMessage.Properties|Bug|
|EMAILJAVA-34707|Exception on adding msg to PST in MAC OS|Bug|
|EMAILNET-39861|MapiCalendar does not save Attendees to ICS|Bug|
|EMAILNET-39842|Multipart/related part marked with content-dispotion attachment missing in MailMessage|Bug|
|EMAILNET-39873|API hangs on exporting MSG to MHTML|Bug|
|EMAILNET-39885|Incorrect parsed EML-File with Aspose.Email|Bug|
|EMAILNET-39874|Colors of text are lost in exported MHT|Bug|

## **New Features**

#### **Render custom icons in message attachment while HTML conversion**
Sometimes, the message contains in-line attachments, that are shown up as icon images in a message body. Such messages may create problems while converting them to HTML, since the icon images are lost. This is because attachment's icons are not held directly in the message.

We have fixed this problem so that the user can customize the icons for attachments when converting the message to HTML. For that, the HtmlSaveOptions.ResourceHtmlRendering event has been added:

{{< highlight java >}}
HtmlSaveOptions options = new HtmlSaveOptions();
options.setResourceHtmlRenderingHandler(new ResourceHtmlRenderingHandler() {
   @Override
   public void invoke(Object sender, ResourceHtmlRenderingEventArgs e) {
        AttachmentBase attachment = (AttachmentBase) sender;
        e.setCaption(attachment.getContentType().getName());
       if (attachment.getContentType().getName().endsWith(".pdf")) {
            e.setPathToResourceFile("pdf_icon.png");
       } else if (attachment.getContentType().getName().endsWith(".docx")) {
            e.setPathToResourceFile("word_icon.jpg");
       } else if (attachment.getContentType().getName().endsWith(".jpg")) {
            e.setPathToResourceFile("jpeg_icon.png");
       } else {
            e.setPathToResourceFile("not_found_icon.png");
       }
   }
});

options.setResourceRenderingMode(ResourceRenderingMode.SubstituteFromFile);
String fileName = "message.msg";
MailMessage mailMessage = MailMessage.load(fileName);
mailMessage.save("fileName.html", options);

{{< /highlight >}}
#### **Get Email Category in MHTML**
We have introduced the ability to add a category header while converting message to MHML.

{{< highlight java >}}
MapiMessage msg = new MapiMessage("from@aaa.com", "to@aaa.com", "subj", "body");
msg.setCategories(new String[] { "Urgently", "Important" });
MhtSaveOptions saveOptions = new MhtSaveOptions();
saveOptions.getFormatTemplates().set_Item(MhtTemplateName.CATEGORIES,
    saveOptions.getFormatTemplates().get_Item(MhtTemplateName.CATEGORIES).replace("Categories", "Les catégories"));

saveOptions.getRenderingHeaders().add(MhtTemplateName.CATEGORIES);
msg.save("fileName.mhtml", saveOptions);
{{< /highlight >}}

#### **Create PST with size more than 2Gb using OutputStream**
The user can optimize PST internal cache using new PersonalStorage API method:

blockSize - The optimal block size to expand cache buffer(in bytes)

{{< highlight java >}}

PersonalStorage create(OutputStream stream, int blockSize, /*FileFormatVersion*/int version)

{{< /highlight >}}

#### **Using Timeout for Countering Endless Wait Operations While Saving Message to MHT Format**
Sometimes, when processing a corrupted message, an operation may be performed infinitely and thus impair the correct functionality of the application.
By using a configurable timeout, you can stop a stuck operation, handle the event, and continue executing the application.

We have added the following members to **MhtSaveOptions** class:

- `MhtSaveOptions.getTimeout, setTimeout` - Limits the time in milliseconds of formatting message. The default value is 3000 milliseconds.
- `MhtSaveOptions.getTimeoutReachedHandler, setTimeoutReachedHandler` - Raised if timed out while saving to MHTML.

Code sample:

{{< highlight java >}}
String emlFileName = "input.eml";
String mhtFileName = "output.mhtml";

MailMessage mailMessage = MailMessage.load(emlFileName);
MhtSaveOptions options = SaveOptions.getDefaultMhtml();
options.setTimeout(4000);
options.setTimeoutReachedHandler(new TimeoutReachedHandler() {
    public void invoke(Object sender, EventArgs e) {
        //handler
    }
});
mailMessage.save(mhtFileName, options);
{{< /highlight >}}

#### **The Try-With-Resources Statement**
We have added a `java.io.Closeable` implementation for all classes that implement `IDisposable`.
{{< highlight java >}}
try (PersonalStorage pst = PersonalStorage.fromFile(fileName, false)) {
    // pst.
}

try (MboxStorageReader reader = MboxStorageReader.createReader("fileName", false)) {
    //reader.
}
{{< /highlight >}}
