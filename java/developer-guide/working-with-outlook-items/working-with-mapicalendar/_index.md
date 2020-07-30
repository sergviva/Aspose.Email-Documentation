---
title: Working with MapiCalendar
type: docs
weight: 110
url: /java/working-with-mapicalendar/
---

Aspose.Email's [MapiCalendar](https://apireference.aspose.com/java/email/com.aspose.email/MapiCalendar) class provides methods and attributes that set various properties of a calendar item.
## **Create and Save Calendar Items**
The following code sample shows creating and saving a calendar item in ICS format.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CalendarItems-CreatAndSaveCalendarItems.java" >}}
### **Save the Calendar Item as ICS**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CalendarItems-SavingTheCalendarItemAsMSG.java" >}}
## **Add Display Reminder to a Calendar**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CalendarItems-AddDisplayReminderToACalendar.java" >}}
## **Add Audio Reminder to a Calendar**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CalendarItems-AddAudioReminderToACalendar.java" >}}
## **Get Recipient Status from MapiCalendar**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CalendarItems-GetRecipientStatusFromMapiCalendar.java" >}}
## **Convert Appointment EML to MSG with HTML Body**
Since version 19.3, Aspose.Email provides the ability to convert Appointment EML to MSG while retaining the HTML body of the appointment. Aspose.Email provides a [MapiConversionOptions.ForcedRtfBodyForAppointment](https://apireference.aspose.com/java/email/com.aspose.email/MapiConversionOptions#setForcedRtfBodyForAppointment\(boolean\))[ ](https://apireference.aspose.com/net/email/aspose.email.mapi/mapiconversionoptions/properties/forcedrtfbodyforappointment)property which has a default value of **true.** When the value of [MapiConversionOptions.ForcedRtfBodyForAppointment](https://apireference.aspose.com/java/email/com.aspose.email/MapiConversionOptions#setForcedRtfBodyForAppointment\(boolean\)) is set to **true**, the appointment body is converted to RTF format. To keep the appointment body format in HTML format, set the value of [MapiConversionOptions.ForcedRtfBodyForAppointment](https://apireference.aspose.com/java/email/com.aspose.email/MapiConversionOptions#setForcedRtfBodyForAppointment\(boolean\)) to **false.**

The following example demonstrates the use of [MapiConversionOptions.ForcedRtfBodyForAppointment](https://apireference.aspose.com/java/email/com.aspose.email/MapiConversionOptions#setForcedRtfBodyForAppointment\(boolean\)) property to keep the appointment body format in HTML format.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-ConvertAppointmentEMLToMSGWithHTMLBody-1.java" >}}
