---
title: Working With Calendar Items on Exchange Server
type: docs
weight: 60
url: /java/working-with-calendar-items-on-exchange-server/
---

## **Sending Meeting Requests**
This article shows how to send a meeting request to multiple recipients using Exchange Web Services and Aspose.Email.

1. Create a meeting request using the Appointment class and set the location, time and attendees.
1. Create an instance of the MailMessage class and set the appointment using the MailMessage.addAlternateView() method.
1. Connect to the Exchange Server and send the meeting request using the send(MailMessage) method.

The EWSClient class can be used to connect to an Exchange Servers with Exchange Web Services (EWS) support. For this to work, the server has to be Exchange Server 2007 or later. The following code snippet shows you how to use EWS to send the meeting requests.



{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchangeews-SendMeetingRequestsUsingExchangeServer-SendMeetingRequestsUsingExchangeServer.java" >}}
## **Working with Calendar Items using EWS**
Aspose.Email provides the capability to add, update and cancel appointments using Exchange Web Service (EWS) client. The IEWSClients CreateAppointment, UpdateAppointment and CancelAppointment methods allow manipulating calendar items using EWS. This article provides detailed code sample of working with Calendar items. The following code sample shows how to:

1. Create an appointment.
1. Update an appointment.
1. Delete/Cancel an appointment.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchangeews-CreatingUpdatingAndDeletingCalendarItemsUsingEWS-CreatingUpdatingAndDeletingCalendarItemsUsingEWS.java" >}}
## **Listing Appointments with Paging Support**
The ListAppointments method exposed by the IEWSClient API retrieves the complete list of appointments from the Exchange server. This may take time if there are large number of appointments on the Exchange Server. The API provides overloaded methods of listAppointmentsByPage method that gives paging support to the operation. This can be used in different combination with querying feature as well. The following overloaded methods are available to list appointments from Exchange Server with Paging support.

- AppointmentPageInfo listAppointmentsByPage(int itemsPerPage)
- AppointmentPageInfo listAppointmentsByPage(int itemsPerPage, int itemOffset)
- AppointmentPageInfo listAppointmentsByPage(MailQuery query, int itemsPerPage)
- AppointmentPageInfo listAppointmentsByPage(MailQuery query, int itemsPerPage, int itemOffset)
- AppointmentPageInfo listAppointmentsByPage(String folderUri, int itemsPerPage)
- AppointmentPageInfo listAppointmentsByPage(String folderUri, int itemsPerPage, int itemOffset)
- AppointmentPageInfo listAppointmentsByPage(String folderUri, MailQuery query, int itemsPerPage)
- AppointmentPageInfo listAppointmentsByPage(String folderUri, MailQuery query, int itemsPerPage, int itemOffset)

The following code snippet shows you how to list appointments with paging support.



{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchangeews-ListAppointmentsWithPagingSupport-ListAppointmentsWithPagingSupport.java" >}}
## **Adding Event to Secondary Calendar folder on Exchange Server**
Aspose.Email API lets you create a secondary Calendar folder on Exchange Server using the IEWSClient. Appointments can then be added, updated or cancelled from the secondary calendar using the createAppointment, updateAppointment and cancelAppointment methods. The following API methods and properties are used in the code samples below to show the functionality of this feature. Please note that this feature is supported from Aspose.Email for .NET 6.5.0 onwards.

- Method IEWSClient.cancelAppointment(Appointment, String).
- Method IEWSClient.cancelAppointment(String, String).
- Method IEWSClient.createAppointment(Appointment, String).
- Method IEWSClient.createFolder(String, String, ExchangeFolderPermissionCollection, String).
- Method IEWSClient.fetchAppointment(String, String).
- Method IEWSClient.updateAppointment(Appointment, String).
- Method IEWSClient.getCurrentCalendarFolderUri()

The following code snippet shows you how to add event to secondary calendar folder on exchange server.



{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchangeews-AddEventToSecondaryCalendar-AddEventToSecondaryCalendar.java" >}}
## **Sharing Calendar Invitation**
Microsoft Exchange server provides the capability to share calendars by sending calendar invitations to other users, registered on the same Exchange server. Aspose.Email API provides the same capability by allowing to share the calendar using the EWS API.



{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchangeews-SendCalendarInvitation-SendCalendarInvitation.java" >}}
## **Retrieving Extended Attributes Information from Calendar Items**
Aspose.Email API lets you retrieve calendar items from Exchange Server. It also supports filtering messages with certain Extended Attributes. This example shows how to retrieve extended attributes information for calendar items on Exchange Server.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-RetreiveExtAttributesForCalendarItems-RetreiveExtAttributesForCalendarItems.java" >}}
