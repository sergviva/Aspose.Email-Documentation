---
title: Working with Outlook Calendar Items
type: docs
weight: 120
url: /java/working-with-outlook-calendar-items/
---

## **Working with MapiCalendar**
Aspose.Email's [MapiCalendar](https://apireference.aspose.com/java/email/com.aspose.email/MapiCalendar) class provides methods and attributes to set various properties of a calendar item. This article provides code samples for:

- [Creating and saving calendar items](#creating-and-saving-calendar-items)
- [Setting reminders for MapiCalendar items](#adding-display-reminder-to-a-calendar)
- [Add/Retrieve Attachments from Calendar](#addretrieve-attachments-from-calendar-files)
- [Retrieving Status of Recipients from Meeting Requests](#status-of-recipients-from-a-meeting-request)
- [Creating MapiCalendar TimeZone object from Standard Timezone](#create-mapicalendartimezone-from-standard-timezone)
### **Creating and Saving Calendar items**
The following code snippet shows you how to create and save a calendar item in ICS format.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CalendarItems-CreatAndSaveCalendarItems.java" >}}
### **Saving the Calendar item as MSG**
The following code snippet shows you how to save the calendar item as MSG.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CalendarItems-SavingTheCalendarItemAsMSG.java" >}}
### **Adding display reminder to a Calendar**
The following code snippet shows you how to add display reminder to a calendar.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CalendarItems-AddDisplayReminderToACalendar.java" >}}
### **Adding audio reminder to a Calendar**
The following code snippet shows you how to add an audio reminder to a calendar.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CalendarItems-AddAudioReminderToACalendar.java" >}}
### **Add/Retrieve attachments from Calendar files**
The following code snippet shows you how to add/retrieve attachments from calendar files.



~~~Java
// For complete examples and data files, please go to https://github.com/aspose-email/Aspose.Email-for-Java
String[] files = new String[3];
files[0] = dataDir + "attachment_1.doc";
files[1] = dataDir + "download.png";
files[2] = dataDir + "Desert.jpg";

Appointment app1 = new Appointment("Home", addHours(new Date(), 1), addHours(new Date(), 1), 
        new MailAddress("organizer@domain.com"), MailAddressCollection.to_MailAddressCollection("attendee@gmail.com"));
for (String file : files)
{
    try (InputStream is = new FileInputStream(file))
    {
        app1.getAttachments().addItem(new Attachment(is, getFileName(file)));
    }
}

app1.save(dataDir + "appWithAttachments_out.ics", AppointmentSaveFormat.Ics);

Appointment app2 = Appointment.load(dataDir + "appWithAttachments_out.ics");
System.out.println(app2.getAttachments().size());
for (Attachment att : app2.getAttachments())
    System.out.println(att.getName());
~~~
### **Status of Recipients from a Meeting Request**
The following code snippet shows you how to status of recipients from a meeting request.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-CalendarItems-GetRecipientStatusFromMapiCalendar.java" >}}
### **Create MapiCalendarTimeZone from Standard Timezone**
The following code snippet shows you how to Create MapiCalendarTimeZone from standard Timezone.



~~~Java
// For complete examples and data files, please go to https://github.com/aspose-email/Aspose.Email-for-Java
MapiCalendarTimeZone timeZone = new MapiCalendarTimeZone("Eastern Standard Time");
~~~
## **Setting Reminder with the Created Appointment**
A reminder can be added when an appointment is created. These alarms can trigger based on different criteria like n minutes before the schedule starts, repeat n times at n intervals. Different tags can be used to create these triggers in the script enclosed by BEGIN:VALARM and END:VALARM within an appointment. There are a number of variants in which the reminder can be set on an appointment.
### **Setting a Reminder by Adding Tags**
The following code snippet shows you how to Set a reminder by adding tags.



~~~Java
// For complete examples and data files, please go to https://github.com/aspose-email/Aspose.Email-for-Java
// The path to the File directory.
String dataDir = RunExamples.getDataDir_Outlook();
long MIN_MS = 60 * 1000;
long HR_MS = 60 * MIN_MS;
long DAY_MS = 24 * HR_MS;

String location = "Meeting Location: Room 5";
Date startDate = getDate(1997, 3, 18, 18, 30, 00);
Date endDate = getDate(1997, 3, 18, 19, 30, 00);
MailAddress organizer = new MailAddress("aaa@amail.com", "Organizer");
MailAddressCollection attendees = new MailAddressCollection();
attendees.addItem(new MailAddress("bbb@bmail.com", "First attendee"));

Appointment target = new Appointment(location, startDate, endDate, organizer, attendees);

// Audio alarm that will sound at a precise time and
// Repeat 4 more times at 15 minute intervals:
AppointmentReminder audioReminder = new AppointmentReminder();
audioReminder.setTrigger(new ReminderTrigger(getDate(1997, 3, 17, 13, 30, 0)));
audioReminder.setRepeat(4);
audioReminder.setDuration(new ReminderDuration(15 * MIN_MS));
audioReminder.setAction(ReminderAction.Audio);
ReminderAttachment attach = new ReminderAttachment(new URI("ftp://Host.com/pub/sounds/bell-01.aud"));
audioReminder.getAttachments().addItem(attach);
target.getReminders().addItem(audioReminder);


// Display alarm that will trigger 30 minutes before the
// Scheduled start of the event it is
// Associated with and will repeat 2 more times at 15 minute intervals:
AppointmentReminder displayReminder = new AppointmentReminder();
ReminderDuration dur = new ReminderDuration(-30 * MIN_MS);
displayReminder.setTrigger(new ReminderTrigger(dur, ReminderRelated.Start));
displayReminder.setRepeat(2);
displayReminder.setDuration(new ReminderDuration(15 * MIN_MS));
displayReminder.setAction(ReminderAction.Display);
displayReminder.setDescription("Breakfast meeting with executive team at 8:30 AM EST");
target.getReminders().addItem(displayReminder);

// Email alarm that will trigger 2 days before the
// Scheduled due date/time. It does not
// Repeat. The email has a subject, body and attachment link.
AppointmentReminder emailReminder = new AppointmentReminder();
ReminderDuration dur1 = new ReminderDuration(-2 * DAY_MS);
emailReminder.setTrigger(new ReminderTrigger(dur1, ReminderRelated.Start));
ReminderAttendee attendee = new ReminderAttendee("john_doe@host.com");
emailReminder.getAttendees().addItem(attendee);
emailReminder.setAction(ReminderAction.Email);
emailReminder.setSummary("REMINDER: SEND AGENDA FOR WEEKLY STAFF MEETING");
emailReminder.setDescription("A draft agenda needs to be sent out to the attendees to the weekly managers meeting (MGR-LIST). Attached is a pointer the document template for the agenda file.");
ReminderAttachment attach1 = new ReminderAttachment(new URI("http://Host.com/templates/agenda.doc"));
emailReminder.getAttachments().addItem(attach1);
target.getReminders().addItem(emailReminder);

// Procedural alarm that will trigger at a precise date/time
// And will repeat 23 more times at one hour intervals. The alarm will
// Invoke a procedure file.
AppointmentReminder procReminder = new AppointmentReminder();
procReminder.setTrigger(new ReminderTrigger(getDate(1998, 1, 1, 5, 0, 0)));
procReminder.setRepeat(23);
procReminder.setDuration(new ReminderDuration(1 * DAY_MS));
procReminder.setAction(ReminderAction.Procedure);
ReminderAttachment attach2 = new ReminderAttachment(new URI("ftp://Host.com/novo-procs/felizano.exe"));
procReminder.getAttachments().addItem(attach2);
target.getReminders().addItem(procReminder);
target.save(dataDir + "savedFile_out.ics");
~~~
## **Convert Appointment EML to MSG with HTML Body**
Since version 19.3, Aspose.Email provides the ability to convert Appointment EML to MSG while retaining the HTML body of the appointment. Aspose.Email provides a [MapiConversionOptions.ForcedRtfBodyForAppointment](https://apireference.aspose.com/java/email/com.aspose.email/MapiConversionOptions#setForcedRtfBodyForAppointment\(boolean\))[ ](https://apireference.aspose.com/net/email/aspose.email.mapi/mapiconversionoptions/properties/forcedrtfbodyforappointment)property which has a default value of **true.** When the value of [MapiConversionOptions.ForcedRtfBodyForAppointment](https://apireference.aspose.com/java/email/com.aspose.email/MapiConversionOptions#setForcedRtfBodyForAppointment\(boolean\)) is set to **true**, the appointment body is converted to RTF format. To keep the appointment body format in HTML format, set the value of [MapiConversionOptions.ForcedRtfBodyForAppointment](https://apireference.aspose.com/java/email/com.aspose.email/MapiConversionOptions#setForcedRtfBodyForAppointment\(boolean\)) to **false.**

The following example demonstrates the use of [MapiConversionOptions.ForcedRtfBodyForAppointment](https://apireference.aspose.com/java/email/com.aspose.email/MapiConversionOptions#setForcedRtfBodyForAppointment\(boolean\)) property to keep the appointment body format in HTML format.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-ConvertAppointmentEMLToMSGWithHTMLBody-1.java" >}}
