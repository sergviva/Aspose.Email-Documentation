---
title: Connecting to Exchange Server
type: docs
weight: 10
url: /net/connecting-to-exchange-server/
---


In order to connect to Exchange servers 2007, 2010 and 2013 using Exchange Web Service, Aspose.Email provides the [IEWSClient](https://apireference.aspose.com/net/email/aspose.email.clients.exchange.webservice/iewsclient) interface that implements the [EWSClient](https://apireference.aspose.com/net/email/aspose.email.clients.exchange.webservice/ewsclient) class. The [EWSClient.GetEWSClient](https://apireference.aspose.com/net/email/aspose.email.clients.exchange.webservice.ewsclient/getewsclient/methods/2) method instantiates and returns an [IEWSClient](https://apireference.aspose.com/net/email/aspose.email.clients.exchange.webservice/iewsclient) object that is further used to perform operations related to an Exchange mailbox and other folders. This article shows how to instantiate objects of [IEWSClient](https://apireference.aspose.com/net/email/aspose.email.clients.exchange.webservice/iewsclient).
## **Connecting to Exchange Server using EWS**
The following code snippet shows you how to connect using Exchange Web Service (EWS).



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-Exchange_EWS-ConnectingToExchangeServerUsingEWS-ConnectingToExchangeServerUsingEWS.cs" >}}
## **Connecting to Exchange Server using IMAP**
Microsoft Exchange Server supports the IMAP protocol for accessing items in a mailbox. Use Aspose.Email's [ImapClient](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient) class to connect to the Exchange Server using the IMAP protocol. For more information about the [ImapClient](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient) class. First, make sure that IMAP services are enabled for your Exchange Server:

1. Open the Control Panel.
1. Go to Administrator Tools, then Services.
1. Check the status of the Microsoft Exchange IMAP4 service.
1. If it is not already running, enable/start it.

The following code snippet shows you how to connect and list messages from the Inbox folder of Microsoft exchange server using IMAP protocol.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-Exchange_EWS-ConnectExchangeServerUsingIMAP-ConnectExchangeServerUsingIMAP.cs" >}}



The following code snippet shows you how to use SSL.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-Exchange_EWS-ExchangeServerUsesSSL-ExchangeServerUsesSSL.cs" >}}



After connecting to an Exchange server using IMAP and getting the [IMapMessageInfoCollection](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapmessageinfocollection), The following code snippet shows you how to use the [MessageInfo](https://apireference.aspose.com/net/email/aspose.email.storage.pst/messageinfo) object's sequence number to save a specific message.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-Exchange_EWS-SaveMessagesUsingIMAP-SaveMessagesUsingIMAP.cs" >}}
