---
title: Working with Gmail Calendars
type: docs
weight: 20
url: /net/working-with-gmail-calendars/
---


## **Adding, Editing and Deleting a Calendar**
Aspose.Email allows applications to manage the Gmail calendars using IGmailClient which provides feature like adding, deleting and updating Gmail calendars. This client class returns list of ExtendedCalendar type objects which contain information about the Gmail calendar items. IGmailClient class exposes following functions for calendars:

- CreateCalendar
  To insert new calendar
- ListCalendars

Get list of all calendars of a client

- DeleteCalendar
  It can be used to delete a calendar
- Fetch Calendar
  It can be used to fetch particular calendar of a client
- Update Calendar
  This function is used for inserting back a modified calendar of a client

To Access the calendars, GoogleTestUser is initialized using gmail account credentials. GoogleOAuthHelper is used to get the access token for the user which is further used to initialize IGmailClient.
### **Insert, Fetch and Update**
For inserting a calendar, initialize a Calendar type object and insert it using CreateCalendar() function. CreateCalendar() returns the id of the newly inserted calendar. This id can be used to fetch the calendar from the server. The following code snippet shows you how to insert, fetch and update calendar.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-InsertFetchAndUpdateCalendar-InsertFetchAndUpdateCalendar.cs" >}}
### **Delete particular calendar**
For deleting a particular calendar, we need to get the list of all the calendars of a client and then delete as required. ListCalendars() returns the list of ExtendedCalendar which contains Gmail calendars. The following code snippet shows you how to delete particular calendar.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-DeleteParticularCalendar-DeleteParticularCalendar.cs" >}}
## **Working with Calendar Access Control**
Aspose.Email provides full control over the access control to the calendar items. ListAccessRules() function is exposed by IGmailClient which returns list of AccessControlRule. Individual rule information can be retrieved, modified and saved back for the calendar of a client. IGmailClient contains following functions for managing the access control rules.

- ListAccessRules
  This function provides list of AccessControlRule
- CreateAccessRule
  This function creates a new access rule for a calendar.
- UpdateAccessRule
  This function is used for updating an access rule.
- FetchAccessRule
  It can be used to fetch particular access rule for calendar of a client
- DeleteAccessRule
  This function is used for deleting an access rule.

The following code snippet shows you how the functions used for managing the access rules:



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-ManageAccessRule-ManageAccessRule.cs" >}}
## **Working with Client Settings and Color Info**
Aspose.Email supports accessing the Client settings by using IGmailClient.GetSettings(). It returns list of settings as given below:

1. dateFieldOrder
1. displayAllTimezones
1. hideInvitations
1. format24HourTime
1. defaultCalendarMode
1. defaultEventLength
1. locale
1. remindOnRespondedEventsOnly
1. alternateCalendar
1. userLocation
1. hideWeekends
1. showDeclinedEvents
1. weekStart
1. weather
1. customCalendarMode
1. timezoneLabel
1. timezone
1. useKeyboardShortcuts
1. country

Similarly color info for clients can also be retrieved using IGmailClient.GetColors(). This color info object returns the list of Foreground colors, background colors and update date and time.
### **Access client settings**
The following code snippet shows you how the functions used for accessing the client settings:



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-AccessClientSettings-AccessClientSettings.cs" >}}
### **Access color info**
The following code snippet shows you how the functions used for accessing the client color settings.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-AccessColorInfo-AccessColorInfo.cs" >}}
## **Working with Appointments**
Aspose.Email provides features for working with Appointments in Google calendars. Following is the list of tasks that can be performed on appointments in google calendar:

1. Add Appointments.
1. Retrieve list off appointments.
1. Retrieve particular appointment.
1. Update an appointment.
1. Move appointment from one calendar to another.
1. Delete appointment.

IGmailClient provides functions like CreateAppointment, FetchAppointment, UpdateAppointment, ListAppointments, MoveAppointment and DeleteAppointment.
### **Adding an appointment**
Following code sample demonstrates the feature of adding an appointment in a calendar. In this sample following steps are followed:

1. Create and insert a calendar.
1. Retrieve list of appointments from a new calendar.
1. Create an appointment.
1. Insert appointment.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-AddingAnAppointment-AddingAnAppointment.cs" >}}
### **Retrieve and update appointment**
Here retrieving and updating of calendar is demonstrated as follows:

1. Rerieve particaulr appointment.
1. Modify the appointment.
1. Update the appointment in calendar.

It is assumed that a calendar with id "calendarId" and appointment unique id "AppointmentUniqueId" are already extracted. The following code snippet shows you how to retrieve and update appointment.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-RetrieveUpdateAppointment-RetrieveUpdateAppointment.cs" >}}
### **Move and Delete appointment**
Appointment can be moved by providing the source calendar, destination calendar and unique id of appointment in the source calendar. The following code snippet shows you how to move and delete appointment.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-MoveAndDeleteAppointment-MoveAndDeleteAppointment.cs" >}}
