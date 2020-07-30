---
title: Working with Contacts On Exchange Server using EWS
type: docs
weight: 70
url: /java/working-with-contacts-on-exchange-server-using-ews/
---

Exchange Server accounts hold more than just email messages. As well as [fetching](/java/fetch-messages-from-an-exchange-server-mailbox/), [moving](/java/working-with-exchange-mailbox-and-messages/#moving-messages-between-folders-using-ews), [sending](/java/working-with-exchange-mailbox-and-messages/#send-email-message-using-ews) and [deleting email messages](/java/working-with-exchange-mailbox-and-messages/#deleting-messages-from-exchange-server) from Exchange Servers, Aspose.Email allows you to work with contacts. This article explains how to retrieve contact information from an Exchange Server directly or using Exchange Web Services. This article also shows how you can list contacts from the Contacts folder or resolve contacts based on contact name.

- Get Contacts from Exchange Server.
- Resolve Contacts using Contact Name.
- Fetch Particular Contact using Contact Id.
## **Adding Contacts to Exchange Server using EWS**
The [EWSClient](http://www.aspose.com/api/java/email/com.aspose.email/classes/EWSClient) class' createContact() method can be used to add [MapiContact](http://www.aspose.com/api/java/email/com.aspose.email/classes/MapiContact) information to an Exchange Server. The createContact() method takes a MapiContact object as an input parameter.

To add contacts to an Exchange Server:

1. Initialize the [EWSClient](http://www.aspose.com/api/java/email/com.aspose.email/classes/EWSClient) with address and credentials.
1. Initialize the [MapiContact](http://www.aspose.com/api/java/email/com.aspose.email/classes/MapiContact) object with NameInfo populated.
1. Call the createContact() method to add the contact to the Exchange Server.

Aspose.Email provides the [EWSClient](http://www.aspose.com/api/java/email/com.aspose.email/classes/EWSClient) class to connect to Microsoft Exchange Server using Exchange Web Services. The code snippets that follow use Exchange Web Services to add contacts to an Exchange Server.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-AddContactsInformation-AddContactsInformation.java" >}}
## **Update Contacts on Exchange Server using EWS**
The IEWSClient's updateContact method can update contact information on Exchange Server.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-UpdateContactInformation-.java" >}}
## **Delete Contacts from Exchange Server using EWS**
The [EWSClient](http://www.aspose.com/api/java/email/com.aspose.email/classes/EWSClient) class provides the deleteContact to access and delete contacts from an Exchange Server's contacts folder. This method takes the contact ID or [MapiContact](http://www.aspose.com/api/java/email/com.aspose.email/classes/MapiContact) as an input parameter.

To delete contacts from an Exchange Server:

1. Initialize the ExchangeWebServiceClient with address and credentials.
1. Delete a contact using its ID.
1. Delete a contact by calling the deleteContact method with Contact as input parameter.
 

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-DeleteContactsInformation-.java" >}}
## **Get Contacts from an Exchange Server**
Aspose.Email provides the [EWSClient](http://www.aspose.com/api/java/email/com.aspose.email/classes/EWSClient) class to connect to Microsoft Exchange Server using Exchange Web Services. The code snippets that follow use Exchange Web Services to read all the contacts.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-GetContactInformation-GetContactsFromAnExchangeServer.java" >}}
## **Fetch Contact by Id**
Aspose.Email API allows to fetch contact from Exchange Server using the contact id.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-GetContactInformation-FetchContactById.java" >}}
## **Resolve Contacts using Contact Name**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-GetContactInformation-ResolveContactsUsingContactName.java" >}}
## **Find Contacts Located in the Global Address List (GAL)**
Aspose.Email provides the IEWSClient interface to find people located in the global address list (GAL) on server. The code snippets that follow use IEWSClient findPeople() to locate all the contacts.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FindPeopleFromGAL.java" >}}
## **Find Contacts Located in the Specified User's Personal Mailbox**
Aspose.Email provides the IEWSClient interface to find contacts located in the specified user's personal mailbox. The code snippets that follow use IEWSClient findPeople() to locate all the contacts.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FindPeople.java" >}}
## **Determine Contact Notes Format**
The Aspose.Email.Mail.Contact.NotesFormat specifies the contacts' notes text format type defined by Aspose.Email.TextFormat enumerator.
