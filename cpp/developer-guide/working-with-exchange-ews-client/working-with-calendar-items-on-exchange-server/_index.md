---
title: Working with Calendar Items on Exchange Server
type: docs
weight: 50
url: /cpp/working-with-calendar-items-on-exchange-server/
---

## **Sending Meeting Requests**
This article shows how to send a meeting request to multiple recipients using Exchange Web Services and Aspose.Email.

1. Create a meeting request using the [Appointment](https://apireference.aspose.com/cpp/email/class/aspose.email.calendar.appointment/) class and set the location, time and attendees.
1. Create an instance of the [MailMessage](https://apireference.aspose.com/cpp/email/class/aspose.email.mail_message/) class and set the appointment using the [MailMessage->AddAlternateView()](https://apireference.aspose.com/cpp/email/class/aspose.email.mail_message/#a479069f1d35b6edbb957ec79358dc605) method.
1. Connect to the Exchange Server and send the meeting request using the [IEWSClient->Send(MailMessage)](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#a02875ffd55c4033e7d88007a9ac2a83c) method.

The [EWSClient](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.e_w_s_client/) class can be used to connect to an Exchange Servers with Exchange Web Services (EWS) support. For this to work, the server has to be Exchange Server 2007 or later. The following code snippet shows you how to use EWS to send the meeting requests.



{{< gist "aspose-com-gists" "525dd06c8783ebb18fb75cfc4b31d1ef" "Examples-Cpp-source-Exchange_EWS-SendMeetingRequestsUsingEWS-SendMeetingRequestsUsingEWS.cpp" >}}
## **Working with Calendar Items using EWS**
Aspose.Email provides the capability to add, update and cancel appointments using Exchange Web Service (EWS) client. The [IEWSClient->CreateAppointment](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#a2ec5d9579cbc48b6c4de13340dd3a9de), [IEWSClient->UpdateAppointment](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#a3ff5e47297a9788859f545134529d892), and [IEWSClient->CancelAppointment](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#ae6dff92768e091756a5c75079b86a1e4) methods allow manipulating calendar items using EWS. This article provides a detailed code sample of working with Calendar items. The following code sample shows how to:

1. Create an appointment.
1. Update an appointment.
1. Delete/Cancel an appointment.



{{< gist "aspose-com-gists" "525dd06c8783ebb18fb75cfc4b31d1ef" "Examples-Cpp-source-Exchange_EWS-CreatingUpdatingAndDeletingCalendarItemsUsingEWS-CreatingUpdatingAndDeletingCalendarItemsUsingEWS.cpp" >}}
## **Listing Appointments with Paging Support**
The [ListAppointments](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#aa085cd2eec127e7ad7387995940ceb9b) method exposed by the [IEWSClient](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/) API retrieves the complete list of appointments from the Exchange server. This may take time if there are a large number of appointments on the Exchange Server. The API provides overloaded methods of [ListAppointmentsByPage](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#a8943e52df21fe5c229311fa2ca1de5c1) method that gives paging support to the operation. This can be used in different combinations with the querying feature as well. The following overloaded methods are available to list appointments from Exchange Server with Paging support.

- [IEWSClient.ListAppointmentsByPage(int itemsPerPage)](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#a8943e52df21fe5c229311fa2ca1de5c1).
- [IEWSClient.ListAppointmentsByPage(string folderUri, int itemsPerPage)](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#ade393bf8ee5f1749680c5c30ae01363e).
- [IEWSClient.ListAppointmentsByPage(MailQuery query, int itemsPerPage)](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#a2c8b23ef2cf54fc479fda202fbd39e39).
- [IEWSClient.ListAppointmentsByPage(string folderUri, MailQuery query, int itemsPerPage)](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#a93d2e5bc6c5fa6e3835bec4e0f2517ba).
- [IEWSClient.ListAppointmentsByPage(int itemsPerPage, int itemOffset)](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#a9313c29124ada205b484f0896120d978).
- [IEWSClient.ListAppointmentsByPage(string folderUri, int itemsPerPage, int itemOffset)](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#a082ae043602b21b0eabc33cb6630380f).
- [IEWSClient.ListAppointmentsByPage(MailQuery query, int itemsPerPage, int itemOffset)](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#af79ef65e5ce453184a915bfcc278a00e).
- [IEWSClient.ListAppointmentsByPage(string folderUri, MailQuery query, int itemsPerPage, int itemOffset)](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#af1438628357188fddaafd15d1c595125).

The following code snippet shows you how to list appointments with paging support.



{{< gist "aspose-com-gists" "525dd06c8783ebb18fb75cfc4b31d1ef" "Examples-Cpp-source-Exchange_EWS-PagingSupportForListingAppointments-PagingSupportForListingAppointments.cpp" >}}
## **Adding Event to Secondary Calendar folder on Exchange Server**
Aspose.Email API lets you create a secondary Calendar folder on Exchange Server using the [IEWSClient](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/). Appointments can then be added, updated or canceled from the secondary calendar using the [IEWSClient->CreateAppointment](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#a1c9a33a384e8625ba440033e506db511), [IEWSClient->UpdateAppointment](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#ac609f10d0a253d378700c8e47df25171), and [IEWSClient->CancelAppointment](https://apireference.aspose.com/cpp/email/class/aspose.email.clients.exchange.web_service.i_e_w_s_client/#aea79688536fddd4f23a67da6911d5e46) methods. 

The following code snippet shows you how to add an event to a secondary calendar folder on the exchange server.



{{< gist "aspose-com-gists" "525dd06c8783ebb18fb75cfc4b31d1ef" "Examples-Cpp-source-Exchange_EWS-SecondaryCalendarEvents-SecondaryCalendarEvents.cpp" >}}
## **Sharing Calendar Invitation**
Microsoft Exchange server provides the capability to share calendars by sending calendar invitations to other users, registered on the same Exchange server. Aspose.Email API provides the same capability by allowing to share the calendar using the EWS API.



{{< gist "aspose-com-gists" "525dd06c8783ebb18fb75cfc4b31d1ef" "Examples-Cpp-source-Exchange_EWS-SendCalendarInvitation-SendCalendarInvitation.cpp" >}}
## **Retrieving Extended Attributes Information from Calendar Items**
{{< gist "aspose-com-gists" "525dd06c8783ebb18fb75cfc4b31d1ef" "Examples-Cpp-source-Exchange_EWS-RetreiveExtAttributesForCalendarItems-RetreiveExtAttributesForCalendarItems.cpp" >}}
