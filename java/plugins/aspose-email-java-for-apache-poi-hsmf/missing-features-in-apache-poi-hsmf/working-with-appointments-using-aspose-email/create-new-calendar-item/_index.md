---
title: Create New Calendar Item
type: docs
weight: 10
url: /java/create-new-calendar-item/
---

## **Aspose.Email - Create New Calendar Item**
Aspose.Email's [MapiCalendar](http://www.aspose.com/docs/display/emailjava/com.aspose.email.MapiCalendar+class) class provides methods and attributes that set various properties of a calendar item.

**Java**

{{< highlight java >}}

 MapiCalendar appointment = new MapiCalendar(

    "Lorem ipsum dolor sit amet.",

    "Appointment",

    "This is a very important meeting :)",

    new Date(2012, 10, 2, 13, 0, 0),

    new Date(2012, 10, 2, 14, 0, 0));

appointment.save(dataDir + "AsposeCalendarItem.ics", AppointmentSaveFormat.Ics);

{{< /highlight >}}
## **Download Running Code**
- [CodePlex](https://asposeemailjavaapachepoi.codeplex.com/releases/view/618811)
- [GitHub](https://github.com/aspose-email/Aspose.Email-for-Java/releases/tag/Aspose.Email_Java_for_Apache_POI-v1.0.0)
## **Download Sample Code**
- [CodePlex](https://asposeemailjavaapachepoi.codeplex.com/SourceControl/latest#src/main/java/com/aspose/email/examples/asposefeatures/appointments/createcalenderitem/AsposeNewCalenderItems.java)
- [GitHub](https://github.com/aspose-email/Aspose.Email-for-Java/tree/master/Plugins/Aspose_Email_for_Apache_POI/src/main/java/com/aspose/email/examples/asposefeatures/appointments/createcalenderitem/AsposeNewCalenderItems.java)

{{% alert color="primary" %}} 

For more details, visit [Working with MapiCalendar](/java/working-with-mapicalendar/).

{{% /alert %}}
