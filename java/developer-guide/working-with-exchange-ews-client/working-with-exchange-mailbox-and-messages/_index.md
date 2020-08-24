---
title: Working with Exchange Mailbox and Messages
type: docs
weight: 90
url: /java/working-with-exchange-mailbox-and-messages/
---

## **Getting Mailbox Information**
If you want to connect to the Exchange Server using Exchange Web Services (EWS), use the ExchangeWebServiceClient class in the Aspose.Email.Exchange namespace. This class uses EWS to connect to and manage items on an Exchange Server.

The code snippets below show how to get mailbox information using the Exchange Web Services.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-GetMailboxInformationFromExchangeServer-GetMailboxInformationFromExchangeWebServices.java" >}}
## **Listing Messages**


{{% alert color="primary" %}} 

A list of the email messages in an Exchange mailbox can be fetched by calling the listMessages() method. Get the basic information about messages, such as subject, from, to and message ID, using the listMessage() method.

This article shows how to connect to an Exchange Server and list the emails in a mailbox using Exchange Web Services. It further shows how to list messages from different folders and how to list messages by ID.

{{% /alert %}} {{% alert color="primary" %}} 

For connecting to exchange server, please refer to the link Connecting to Exchange Server.

{{% /alert %}} 
### **List Exchange Server Messages using EWS**
The code snippets below connects to an Exchange Server using EWS and lists messages from the Inbox folder:

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-ListMessages-ListMessagesFromInboxFolderOnExchangeServerUsingEWS.java" >}}
### **Listing Messages from Different Folders with EWS**
Alternatively, if you want to list messages using Exchange Web Services, use the ExchangeWebService class instead of the ExchangeClient class. The code snippets below use EWS:

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-ListMessages-ListMessagesFromOtherFoldersOnExchangeServerUsingEWS.java" >}}
### **Listing Messages with Paging Support**
Aspose.Email provides the capability to fetch messages from Exchange server based on multiple server responses.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FetchMessagesFromAnExchangeServerMailbox-EnumerateMessagesWithPagingInEWS.java" >}}
### **Listing Messages by Extended Properties**
In order to list messages having certain extended properties, the overloaded method of ListMessages can be used as shown in code sample below.

``` java

 IEWSClient client = EWSClient.getEWSClient("https://outlook.office365.com/ews/exchange.asmx", "Shabir.haider@studentpartner.com", "LoveAir1993");

{

    try

    {

        List<String> extendedProperties = new List<String>();

        extendedProperties.add("blablaprop");

        ExchangeMessageInfoCollection messageInfoCol = client.listMessages(

                client.getMailboxInfo().getInboxUri(),

                ExchangeListMessagesOptions.FetchAttachmentInformation,

                extendedProperties);

    }

    finally

    {

    }

}

```
### **Getting Message Class Information from ExchangeMessageInfo**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchangeews-GetMessageClassInformationUsingEWS-GetMessageClassInformationUsingEWS.java" >}}
## **Reading Emails from Other User's Mailbox with EWS**
{{% alert color="primary" %}} 

Some accounts on Exchange Servers have the right to access multiple mailboxes, and some users have multiple email accounts on the same Exchange Server. In both cases, users can access other user's mailboxes using Aspose.Email for Java. This API provides mechanism for accessing folders and emails from other mailboxes using the ExchangeWebServiceClient class.

{{% /alert %}} {{% alert color="primary" %}} 

This functionality can be achieved using the overloaded getMailboxInfo() method and providing the user email address as a parameter.

{{% /alert %}} 

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-ReadEmailsFromOtherUsersMailbox-UsingExchangeWebServiceClient.java" >}}
## **Send Email Message using EWS**
You can send email messages using an Exchange Server with the help of the tools in com.aspose.email. The IEWSClient.send() method accepts a [MailMessage](http://www.aspose.com/api/java/email/com.aspose.email/classes/MailMessage) instance as a parameter and sends the email. Aspose.Email provides the IEWSClient class to connect to Microsoft Exchange Server using Exchange Web Services. The code snippets that follow uses EWS to send emails using Microsoft Exchange Server.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-SendEmailMessageUsingExchangeServer-SendEmailMessageUsingExchangeServerUsingEWS.java" >}}
## **Get ExchangeMessageInfo From Message URI**


{{% alert color="primary" %}} 

An email message is represented by its unique identifier, URI, and is integral part of the [ExchangeMessageInfo](http://www.aspose.com/api/java/email/com.aspose.email/classes/ExchangeMessageInfo) object. In case, only message URI is available, then [ExchangeMessageInfo](http://www.aspose.com/api/java/email/com.aspose.email/classes/ExchangeMessageInfo) object can also be retrieved using this available information. The overload version of ListMessages takes a list of Ids to use [ExchangeMessageInfoCollection](http://www.aspose.com/api/java/email/com.aspose.email/classes/ExchangeMessageInfoCollection).

{{% /alert %}} 

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-GetExchangeMessageInfoFromMessageURI-.java" >}}
## **Pre-Fetch Message Size using Aspose.Email IEWSClient**
{{% alert color="primary" %}} 

Microsoft Outlook InterOp provides the feature of retrieving message size before actually fetching the complete message from the server. In case of Aspose.Email API, the summary information retreived from Exchange server is represented by [ExchangeMessageInfo](http://www.aspose.com/api/java/email/com.aspose.email/classes/ExchangeMessageInfo) class. It provides the same feature of retrieving message size using the Size property.

{{% /alert %}} 

In order to retrieve the message size, the standard call to IEWClient's ListMessages is used that retrieves collection of [ExchangeMessagInfo](http://www.aspose.com/api/java/email/com.aspose.email/classes/ExchangeMessageInfo). The following sample code provides an example of displaying message size using the [ExchangeMessageInfo](http://www.aspose.com/api/java/email/com.aspose.email/classes/ExchangeMessageInfo) class.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-PreFetchMessageSize-.java" >}}
## **Saving Messages**
This article shows how to get messages from an Exchange Server mailbox and save them to disk in EML and MSG formats.
### **Save Messages from Exchange Server Mailbox to EML**
To save messages using Exchange Web Services, use the ExchangeWebServiceClient class can be used. The following code snippets use EWS to connect to the Exchange Server and save messages as EML files.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-SaveMessagesFromExchangeServerMailbox-SaveMessagesAsEMLUsingEWS.java" >}}
### **Save Messages to an OutputStream**
Instead of saving EML files to disk, it is possible to save it to an OutputStream. This is useful when you want to save the stream to some storage location like a database. Once the stream has been saved to a database, you can reload the EML file into the MailMessage class.

The code snippets below save messages from an Exchange Server mailbox to a memory stream. When using Exchange Web Services, the following code can be used to save the message to a stream.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-SaveMessagesFromExchangeServerMailbox-SaveMessagesToOutputStreamUsingEWS.java" >}}
### **Save Messages in MSG Format**
Messages can also be saved in MSG format using EWS using the ExchangeWebServiceClient class, which is part of the com.aspose.email namespace. The following code snippets save the messages to MSG on disk using EWS.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-SaveMessagesFromExchangeServerMailbox-SaveMessagesInMSGFormatUsingEWS.java" >}}
## **Moving Messages between Folders using EWS**
You can move email messages from one folder to another with the help of the [I](http://www.aspose.com/api/java/email/com.aspose.email/classes/ExchangeClient)EWSClient.moveItem() method. It takes the parameters:

- The unique URI of the message which is to be moved.
- The unique URI of the destination folder.

The sample code below moves a message in a mailbox from the Inbox folder to a folder called Processed. In this example, the application:

1. Reads messages from the Inbox folder.
1. Processes some of the messages based on some criteria (in this example, we find a keyword in the message subject).
1. Moves messages which fulfill the given condition to the Processed folder.
 

Aspose.Email provides the ExchangeWebServiceClient class to connect to Microsoft Exchange Server using Exchange Web Services. The code snippets that follow use Exchange Web Services to move messages from the Inbox folder to the Processed folder.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-MoveMessageFromOneFolderToAnother-MoveMessagesBetweenFoldersUsingEWS.java" >}}
## **Copy Messages From One Folder to Other using EWS**
{{% alert color="primary" %}} 

Aspose.Email API allows to copy a message from one folder to another folder using the copyItem method. The overloaded version of this method returns the Unique URI of the copied message as shown in this article.

{{% /alert %}} 

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-CopyAMessageToAnotherFolder-.java" >}}
## **Deleting Messages from Exchange Server**
You can delete email messages from a folder with the help of the IEWSClient.deleteMessage() method. It takes the message's unique URI as a parameter.

The sample code below deletes a message from the Inbox folder. For the purpose of this example, the code:

1. Reads messages from the Inbox folder.
1. Process messages based on some criteria (in this example, we find a keyword in the message subject).
1. Delete the message.
 

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-DeleteMessagesFromExchangeServer-DeleteMessagesFromExchangeServerUsingEWS.java" >}}
