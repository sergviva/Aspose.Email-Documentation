---
title: Connecting to IMAP Server
type: docs
weight: 10
url: /net/connecting-to-imap-server/
---


The [ImapClient](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient) class allows applications to manage IMAP mailboxes using the IMAP protocol. The [ImapClient](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient) class is used to connect to IMAP mail servers and manage emails in the IMAP email folders. To connect to an IMAP server

1. Create an instance of the [ImapClient](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient) class.
1. Specify the hostname, username, and password in the [ImapClient constructor](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient/constructors/8).

Once the [ImapClient](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient) instance is initiated, the next call to any operation using this instance will connect to the server. The following code snippet shows you how to connect to an IMAP server using the steps above.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-IMAP-ConnectingWithIMAPServer-ConnectingWithIMAPServer.cs" >}}
## **Connecting with SSL Enabled IMAP Server**
[Connecting with IMAP Server](/email/net/connecting-to-imap-server#connecting-with-imap-server) described how to connect to an IMAP server in four simple steps:

1. Create an instance of the [ImapClient](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient) class.
1. Specify the hostname, username, and password.
1. Specify the port.
1. Specify the Security Options.

The process for connecting to an SSL enables IMAP server is similar but requires that you set another few properties:

- Set Security Options to SSLImplicit.

The following code snippet shows how to

1. Set a username, password, and port.
1. Set security option.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-IMAP-SSLEnabledIMAPServer-SSLEnabledIMAPServer.cs" >}}
## **Connecting to Server via Proxy**
Proxy servers are commonly used to communicate with the outside world. In such cases, mail clients are not able to communicate over the Internet without specifying the proxy address. Aspose.Email provides support for versions 4, 4a and 5 of the SOCKS proxy protocol. This article provides a working sample of accessing the mailbox using a proxy mail server. To access the mailbox via a proxy server:

1. Initialize [SocksProxy](https://apireference.aspose.com/net/email/aspose.email.clients/socksproxy) with the required information, that is proxy address, port, and SOCKS version.
1. Initialize [ImapClient](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient) with host address, user name, password, and any other settings.
1. Set the client's [SocksProxy](https://apireference.aspose.com/net/email/aspose.email.clients/socksproxy) property to the [SocksProxy](https://apireference.aspose.com/net/email/aspose.email.clients/socksproxy) object created above.

The following code snippet shows you how to retrieve mailbox via a proxy server.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-IMAP-AccessMailboxViaProxyServer-AccessMailboxViaProxyServer.cs" >}}
## **Connecting to Server via HTTP Proxy**
{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-IMAP-AccessMailboxViaHTTPProxy-AccessMailboxViaHTTPProxy.cs" >}}
## **Connecting to Server in Read-Only mode**
The [ImapClient](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient) class provides a [ReadOnly](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient/properties/readonly) property which when set to **true**, indicates that no changes should be made to the permanent state of the mailbox. The following code sample demonstrates the use of [ImapClient.ReadOnly](https://apireference.aspose.com/net/email/aspose.email.clients.imap/imapclient/properties/readonly) property. It gets the count of unread messages, then fetches one message and then gets the count of unread messages again in read-only mode. The count of the unread messages remains the same indicating that the permanent state of the mailbox was not changed.



{{< gist "aspose-com-gists" "522d47278b8ca448dc1d7eb97193322c" "Examples-CSharp-IMAP-ImapReadOnlyMode-1.cs" >}}
