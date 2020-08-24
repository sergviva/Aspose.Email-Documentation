---
title: Creating Audio Reminder
type: docs
weight: 50
url: /java/creating-audio-reminder/
---

## **Aspose.Email - Creating Audio Reminder**
Adding Audio Reminder to a Calendar

**Java**

``` java

 Calendar calendar = Calendar.getInstance(TimeZone.getTimeZone("GMT"));

calendar.set(2012, Calendar.NOVEMBER, 1, 0, 0, 0);

Date startDate = calendar.getTime();

calendar.set(2012, Calendar.DECEMBER, 1);

Date endDate = calendar.getTime();

MailAddressCollection attendees = new MailAddressCollection();

attendees.addMailAddress(new MailAddress("attendee_address@domain.com", "Attendee"));

WeeklyRecurrencePattern expected = new WeeklyRecurrencePattern(3);

Appointment app = new Appointment("Appointment Location", "Appointment Summary", "Appointment Description",

									startDate, endDate,

									new MailAddress("organizer_address@domain.com", "Organizer"), attendees, expected);

MailMessage msg = new MailMessage();

msg.addAlternateView(app.requestApointment());

MapiMessage mapi = MapiMessage.fromMailMessage(msg);

MapiCalendar cal = (MapiCalendar)mapi.toMapiMessageItem();

cal.setRemainderSet(true);

cal.setRemainderDelta(58);//58 min before start of event

cal.setReminderFileParameter("data/logon.wav");

cal.save("data/AsposeAudioReminder.ics", AppointmentSaveFormat.Ics);

```
## **Download Running Code**
Download **Creating Audio Reminder** form any of the below mentioned social coding sites:

- [CodePlex](https://asposeapachepoi.codeplex.com/downloads/get/1381613)
- [SourceForge](http://sourceforge.net/projects/asposeforapachepoi/files/Aspose.Email%20Features%20Not%20in%20Apache%20POI%20HSMF%20for%20Outlook/Audio%20Reminders%20%28Aspose.Email%29.zip/download)
- [GitHub](https://github.com/asposemarketplace/Aspose_for_Apache_POI/releases/download/More-Features-in-Aspose.Email-v1.1/Audio.Reminders.Aspose.Email.zip)
- [BitBucket](https://bitbucket.org/asposemarketplace/aspose-for-apache-poi/downloads/Audio%20Reminders%20\(Aspose.Email\).zip)

{{% alert color="primary" %}} 

For more details, visit [Working with MapiCalendar](/java/working-with-mapicalendar/).

{{% /alert %}}
