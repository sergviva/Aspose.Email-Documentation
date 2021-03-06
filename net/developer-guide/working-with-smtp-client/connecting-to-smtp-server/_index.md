---
title: Connecting to SMTP Server
type: docs
weight: 10
url: /net/connecting-to-smtp-server/
---


The following properties need to be set when connecting with an SMTP server with SSL support.

- [SecurityOptions](https://apireference.aspose.com/net/email/aspose.email.clients/securityoptions)
- Port

In the examples below we show how to:

1. Set a username.
1. Set a password.
1. Set the port.
1. Set security option.

The following code snippet shows you how to connect SSL enabled SMTP server.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-SSLEnabledSMTPServer-SSLEnabledSMTPServer.cs" >}}
## **Connecting to Server via Socks Proxy Sever**
Sometimes we use proxy servers for communicating with the outside world. In such cases, mail clients are not able to communicate over the Internet without specifying the proxy address. Aspose.Email provides support for versions 4, 4a and 5 of SOCKS proxy protocol. This article provides a working sample of sending email using a proxy mail server. To send an email via a proxy server:

1. Initialize Proxy with the required information, that is proxy address, port, and SOCKS version.
1. Initialize [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) with the host address, user name and password, and any other settings.
1. Set the client's Proxy property to the [Proxy](https://apireference.aspose.com/net/email/aspose.email.clients/proxy) object created earlier.

The following code snippet shows you how to connect to a server via proxy server.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-SendEmailViaProxyServer-SendEmailViaProxyServer.cs" >}}
## **Connecting to Server via HTTP Proxy Server**
{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-SendEmailViaHttpProxy-SendEmailViaHttpProxy.cs" >}}
## **Loading SMTP Authentication Information from CONFIG File**
The [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient)[](http://www.aspose.com/api/net/email/aspose.email.mail/smtpclient) class allows applications to read authentication information like username and password and the host address and port number directly from a configuration file. Using the .NET native configuration tag, as shown below, enables the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class to read this information through the Configuration Manager also available in .NET framework. For Aspose.Email to be able to read a configuration file, it needs to be in the correct format. Below, we show an example XML configuration file followed by the code that reads it. The following code snippet shows you how to load SMTP authentication information from CONFIG File.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "LoadingAuthenticationInformationFromAFile.xml" >}}



Once the configuration settings are defined, load these settings directly into an instance of the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) class using one of its overloaded constructors. The following code snippet demonstrates reading configuration settings from the configuration file and loading them directly into the instance of the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient).



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-LoadSmtpConfigFile-LoadSmtpConfigFile.cs" >}}
## **Bind SMTP Client to Specific IP Address on Host**
The possibility of a host having multiple ports available for sending out emails cannot be ruled out. In such cases, the requirement may arise to bind the email sending client to a specific port on the host for sending out emails. This can be achieved with Aspose.Email API as well using the [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) [BindIPEndPoint](https://apireference.aspose.com/net/email/aspose.email.clients/emailclient/events/bindipendpoint) property. The API's [SmtpClient](https://apireference.aspose.com/net/email/aspose.email.clients.smtp/smtpclient) can be set to use a specific IP address on the host by specifying the specific IP Endpoint. The following code snippet shows you how to bind SMTP Client to Specific IP Address on Host.



{{< gist "aspose-com-gists" "6e5185a63aec6fd70d83098e82b06a32" "Examples-CSharp-SMTP-SetSpecificIpAddress-SetSpecificIpAddress.cs" >}}
