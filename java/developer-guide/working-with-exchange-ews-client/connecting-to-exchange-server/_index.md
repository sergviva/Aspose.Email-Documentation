---
title: Connecting to Exchange Server
type: docs
weight: 10
url: /java/connecting-to-exchange-server/
---

## **Connect to Exchange Server using Exchange Web Service (EWS)**
{{% alert color="primary" %}} 

In order to connect to Exchange servers 2007, 2010 and 2013 using Exchange Web Service, it provides the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) interface that implements the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/EWSClient) class. The [EWSClient.getEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/EWSClient#getEWSClient\(int,%20boolean,%20java.lang.String,%20java.lang.String,%20com.aspose.ms.System.Net.ICredentials,%20com.aspose.ms.System.Net.WebProxy\)) method instantiates and returns an [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) object that is further used to perform operations related to an Exchange mailbox and other folders. This article shows how to instantiate objects of both classes and the same method can be used in all the upcoming examples in this programming guide.

{{% /alert %}} 

The following code sample shows how to connect to Exchange Server using EWS.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ConnectToExchangeServer-GetEWSClient.java" >}}
## **Connect to an Exchange Server using IMAP**
{{% alert color="primary" %}} 

Microsoft Exchange Server supports the IMAP protocol for accessing items in a mailbox. Use Aspose.Email's [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class to connect to the Exchange Server using the IMAP protocol. This article shows how.

{{% /alert %}} {{% alert color="primary" %}} 

For more information about the [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class, read Managing Emails with IMAP.

{{% /alert %}} 


First, make sure that IMAP services are enabled for your Exchange Server:

1. Open the **Control Panel**.
1. Go to **Administrator Tools**, then **Services**.
1. Check the status of the **Microsoft Exchange IMAP4** service.
1. If it is not already running, enable/start it.

Below is the sample source code to connect and list messages from the Inbox folder of Microsoft Exchange Server using the IMAP protocol.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ConnectToExchangeServerUsingIMAP-ConnectToExchangeServerUsingIMAP.java" >}}
### **Programming Sample - Saving One Message Only**
After connecting to an Exchange server using IMAP and getting the [IMapMessageInfoCollection](https://apireference.aspose.com/java/email/com.aspose.email/ImapMessageInfoCollection), you can use the [MessageInfo](https://apireference.aspose.com/java/email/com.aspose.email/MessageInfo) object's sequence number to save a specific message as follow:

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ConnectToExchangeServerUsingIMAP-UseMessageInfoObjectSequenceNumberToSaveAMessage.java" >}}
