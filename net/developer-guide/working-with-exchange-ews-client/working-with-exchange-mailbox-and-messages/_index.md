---
title: Working with Exchange Mailbox and Messages
type: docs
weight: 20
url: /net/working-with-exchange-mailbox-and-messages/
---


## **Getting Mailbox Information Using EWS**
The [EWSClient](https://apireference.aspose.com/net/email/aspose.email.clients.exchange.webservice/ewsclient) class has members that can be used to get mailbox information from an Exchange Server by calling the IEWSClient.GetMailboxInfo() method. It returns an instance of type [ExchangeMailboxInfo](https://apireference.aspose.com/email/net/aspose.email.clients.exchange/exchangemailboxinfo). Get mailbox information from properties such as [MailboxUri](https://apireference.aspose.com/email/net/aspose.email.clients.exchange/exchangemailboxinfo/properties/mailboxuri), [InboxUri](https://apireference.aspose.com/email/net/aspose.email.clients.exchange/exchangemailboxinfo/properties/inboxuri) and [DraftsUri](https://apireference.aspose.com/email/net/aspose.email.clients.exchange/exchangemailboxinfo/properties/draftsuri). This article shows how to access mailbox information using Exchange Web Services.

If you want to connect to the Exchange Server using Exchange Web Services (EWS), use the IEWSClient class in the Aspose.Email.Exchange namespace. This class uses EWS to connect to and manage items on an Exchange Server. The following code snippet shows you how to get mailbox information using the exchange web services.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-GetMailboxInformationFromExchangeWebServices-GetMailboxInformationFromExchangeWebServices.cs" >}}
## **Sending Email Messages**
You can send email messages using an Exchange Server with the help of the tools in [Aspose.Email.Exchange](#working-with-exchange-mailbox-and-messages). The IEWSClient.Send() method accepts a [MailMessage](https://apireference.aspose.com/email/net/aspose.email/mailmessage) instance as a parameter and sends the email. This article explains how to send email messages using Exchange Web Services.

Aspose.Email provides the IEWSClient class to connect to Microsoft Exchange Server using Exchange Web Services. The following code snippet shows you how to uses EWS to send emails using Microsoft Exchange Server. The following code snippet shows you how to sends email messages using EWS.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-SendEmailMessagesUsingExchangeWebServices-SendEmailMessagesUsingExchangeWebServices.cs" >}}
## **Getting Sent Item Uri**
Sent email's Id can be retrieved from Exchange server with the following sample code. This alos uses 

{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-GetUriOfSentEmail-GetUriOfSentEmail.cs" >}}

where the delegate method is:

{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-GetUriOfSentEmail-GetUriOfSentEmailSentHandler.cs" >}}
## **Reading Emails from other User’s Mailbox**
Some accounts on Exchange Servers have the right to access multiple mailboxes, and some users have multiple email accounts on the same Exchange Server. In both cases, users can access other user's mailboxes using Aspose.Email for .NET. This API provides mechanism for accessing folders and emails from other mailboxes using the IEWSClient class. This functionality can be achieved using the overloaded [GetMailboxInfo()](https://apireference.aspose.com/email/net/aspose.email.clients.exchange.dav/exchangeclient/methods/getmailboxinfo) method and providing the user email address as a parameter.

The following code snippet shows you how to reading emails using IEWSClient class.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-AccessAnotherMailboxUsingExchangeWebServiceClient-AccessAnotherMailboxUsingExchangeWebServiceClient.cs" >}}
## **Listing Messages**
A list of the email messages in an Exchange mailbox can be fetched by calling the IEWSClient.ListMessage method. Get the basic information about messages, such as subject, from, to and message ID, using the ListMessage method.
### **Simple Messages Listing**
To list the messages in an Exchange mail box:

1. Create an instance of the [IEWSClient](http://www.aspose.com/api/net/email/aspose.email.exchange/exchangeclient) class.
1. Call the ListMessage method and create a message collection.
1. Loop through the collection and display message information.

The following code snippet shows you how to connects to an exchange server using EWS and lists messages from the inbox folder.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-ListingMessagesUsingEWS-ListingMessagesUsingEWS.cs" >}}
### **Listing Messages From Different Folders**
[The above code snippets](#simple-messages-listing), list all the messages in the Inbox folder. Its possible to get the list of messages from other folders as well. The IEWSClient.ListMessages() method accepts a folder URI as a parameter. As long as the folder URI is valid, you can get the list of messages from that folder. Use the IEWSClient.MailboxInfo.xxxFolderUri property to get the URI of different folders. The rest of the code is same as for getting a list of messages. The following code snippet shows you how to listing messages from different folders using EWS.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-ListingMessagesFromFolders-ListingMessagesFromFolders.cs" >}}
### **Listing Messages with Paging Support**
The following code snippet shows you how to get a list of messages with paging support.

{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-PagingSupportForListingMessages-PagingSupportForListingMessages.cs" >}}
### **Getting Message Type Information from ExchangeMessageInfo**
{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-GetMessageTypeFromExchangeMessageInfo-GetMessageTypeFromExchangeMessageInfo.cs" >}}
## **Saving Messages**
This article shows how to get messages from an Exchange Server mailbox and save them to disk in EML and MSG formats:

- Save as EML on disk.
- Save to memory stream.
- Save as MSG.
### **Saving Messages to EML**
To get messages and save in EML format:

1. Create an instance of the IEWSClient class.
1. Provide the mailboxUri, username, password and domain.
1. Call the IEWSClient.ListMessages() method to get an instance of the ExchangeMessagesInfoCollection collection.
1. Loop through the ExchangeMessagesInfoCollection collection to get the unique URI for each message.
1. Call the IEWSClient.SaveMessage() method and pass the unique URI as a parameter.
1. Provide a the SaveMessage() method with a path to where you want to save the file.

The following code snippet shows you how to use EWS to connect to the Exchange Server and save messages as EML files.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-SaveMessagesUsingExchangeWebServices-SaveMessagesUsingExchangeWebServices.cs" >}}
### **Saving Messages to a Memory Stream**
Instead of saving EML files to disk, it is possible to save it to a memory stream. This is useful when you want to save the stream to some storage location like a database. Once the stream has been saved to a database, you can reload the EML file into the [MailMessage](https://apireference.aspose.com/email/net/aspose.email/mailmessage) class. The following code snippet shows you how to save messages from an Exchange Server mailbox to a memory stream using EWS.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-SaveMessagesToMemoryStreamUsingEWS-SaveMessagesToMemoryStream.cs" >}}
### **Saving Messages in MSG Format**
The IEWSClient.SaveMessage() method can directly save the message to EML format. To save the messages to MSG format, first call the IEWSClient.FetchMessage() method which returns an instance of the [MailMessage](https://apireference.aspose.com/email/net/aspose.email/mailmessage) class. Then call the MailMessage.Save() method to save the message to MSG. The following code snippet shows you how to gets messages from an Exchange Server mailbox and saves them to MSG format using EWS.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-SaveMessagesInMSGFormatExchangeEWS-SaveMessagesInMSGFormatExchangeEWS.cs" >}}
## **Getting ExchangeMessageInfo from Message URI**
An email message is represented by its unique identifier, URI, and is integral part of the ExchangeMessageInfo object. In case, only message URI is available, then ExchangeMessageInfo object can also be retrieved using this available information. The overload version of ListMessages takes a list of Ids to use ExchangeMessageInfoCollection. The following code snippet shows you how to get ExchangeMessageInfo from message URI.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-GetExchangeMessageInfoFromMessageURI-GetExchangeMessageInfoFromMessageURI.cs" >}}
## **Fetch Messages from an Exchange Server Mailbox**
Listing Messages on an Exchange Server used the ListMessages() method to get a list of messages from an Exchange Server mailbox. The ListMessage() method gets basic information about messages, for example, the subject, the message ID, from and to. To get the complete message details, Aspose.Email.Exchange provides the IEWSClient.FetchMessage() method. This method accepts the message URI as a parameter and returns am instance of the Aspose.Emai.Mail.MailMessage class. The MailMessage class then provides message details like body, headers and attachments. Find out more about the MailMessage API, or find out how to manage emails with the MailMessage class. To fetch messages from Exchange Server Mailbox:

1. Create an instance of type IEWSClient.
1. Specify the server name, user name, password and domain.
1. Call ListMessages to get the ExchangeMessageInfoCollection.
1. Loop through the ExchangeMessageInfoCollection collection to get ExchangeMessageInfo.UniqueURI values.
1. Call IEWSClient.FetchMessage() and pass ExchangeMessageInfo.UniqueURI() as parameter.

The following code snippet shows you connect to the Exchange Server mailbox and fetches all the messages using EWS.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-FetchMessageUsingEWS-FetchMessageUsingEWS.cs" >}}
## **Pre-Fetch Message Size**
Microsoft Outlook InterOp provides the feature of retrieving message size before actually fetching the complete message from the server. In case of Aspose.Email API, the summary information retreived from Exchange server is represented by ExchangeMessageInfo class. It provides the same feature of retrieving message size using the Size property. In order to retrieve the message size, the standard call to IEWSClient's ListMessages is used that retrieves collection of ExchangeMessagInfo. The following code snippet shows you how to display message size using the ExchangeMessageInfo class.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-PreFetchMessageSizeUsingIEWSClient-PreFetchMessageSizeUsingIEWSClient.cs" >}}
## **Download Messages Recursively**
The [EWSClient](https://apireference.aspose.com/net/email/aspose.email.clients.exchange.webservice/ewsclient)’s [ListSubFolders()](https://apireference.aspose.com/email/net/aspose.email.clients.exchange.dav/exchangeclient/methods/listsubfolders/index) method can be used to get messages from folders and subfolders from an Exchange Server mailbox recursively. This requires Exchange Server 2007 or greater, because it uses EWS. The following code snippet shows you how to download the whole mailbox (folders and subfolders) of an Exchange Server. The folder structure is created locally and all messages download.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-DownloadMessagesFromExchangeServerFoldersRecursively-DownloadMessagesFromExchangeServerFoldersRecursively.cs" >}}
## **Download Messages from Public Folders**
Microsoft Exchange Server lets users create public folders and post messages in them. To do this through your application, use Aspose.Email's [EWSClient](https://apireference.aspose.com/net/email/aspose.email.clients.exchange.webservice/ewsclient) class to connect to the Exchange Server and read and download messages and posts from public folders. The following code snippet shows you how to reads all public folders, and subfolders, and lists and downloads any messages found in these folders. This example only works with Microsoft Exchange Server 2007 or above since only these support EWS.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-DownloadMessagesFromPublicFolders-DownloadMessagesFromPublicFolders.cs" >}}
## **Moving Messages**
You can move email messages from one folder to another with the help of the IEWSClient class Move method. It takes the parameters:

- The unique URI of the message which is to be moved.
- The unique URI of the destination folder.
### **Moving Messages between Folders**
The following code snippet shows you how to move a message in a mailbox from the Inbox folder to a folder called Processed. In this example, the application:

1. Reads messages from the Inbox folder.
1. Processes some of the messages based on some criteria (in this example, we find a keyword in the message subject).
1. Moves messages which fulfill the given condition to the processed folder.

{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-MoveMessageFromOneFolderToAnotherusingEWS-MoveMessageFromOneFolderToAnotherusingEWS.cs" >}}
## **Deleting Messages**
You can delete email messages from a folder with the help of the ExchangeClient class DeleteMessage method. It takes the message's unique URI as a parameter.

The following code snippet shows you how to delete a message from the Inbox folder. For the purpose of this example, the code:

1. Reads messages from the Inbox folder.
1. Process messages based on some criteria (in this example, we find a keyword in the message subject).
1. Deletes the message.

{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-DeleteMessagesFromUsingEWS-DeleteMessagesFromusingEWS.cs" >}}
## **Copying Messages**
Aspose.Email API allows to copy a message from one folder to another folder using the CopyItem method. The overloaded version of this method returns the Unique URI of the copied message as shown in this article.
### **Copying a Message to Another Folder**
The following code snippet shows you how to copy a message to another folder.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Exchange_EWS-CopyingMessageToAnotherFolder-CopyingMessageToAnotherFolder.cs" >}}
