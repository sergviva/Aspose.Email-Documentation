---
title: Connecting to SMTP Server
type: docs
weight: 10
url: /java/connecting-to-smtp-server/
---

## **Connecting to Server via Proxy Server**
Sometimes we use proxy servers for communicating with the outside world. In such cases, mail clients are not able to communicate over the Internet without specifying the proxy address. Aspose.Email provides support for versions 4, 4a and 5 of SOCKS proxy protocol. This article provides a working sample of sending email using a proxy mail server. To send an email via a proxy server:

1. Initialize [SocksProxy](https://apireference.aspose.com/java/email/com.aspose.email/SocksProxy) with the required information, that is proxy address, port, and SOCKS version.
1. Initialize [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient) with the host address, user name and password, and any other settings.
1. Set the client's [SocksProxy](https://apireference.aspose.com/java/email/com.aspose.email/EmailClient#setSocksProxy\(com.aspose.email.SocksProxy\)) property to the [SocksProxy](https://apireference.aspose.com/java/email/com.aspose.email/SocksProxy) object created earlier.

The following code snippet shows you how to connect to a server via a proxy server.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-smtp-SendEmailViaProxyServer-.java" >}}
## **Connecting to SMTP Server via HTTP Proxy Server**
Aspose.Email lets you connect to the SMTP server via HTTP Proxy as shown in the following code sample.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-smtp-SendEmailViaProxyServer-SendEmailViaHttpProxy.java" >}}
## **Binding SMTP Client to Specific IP Address on Host**
The possibility of a host having multiple ports available for sending out emails cannot be ruled out. In such cases, the requirement may arise to bind the email sending client to a specific port on the host for sending out emails. This can be achieved with Aspose.Email APIs as well using the [SmtpClient.bindIPEndPoint](https://apireference.aspose.com/java/email/com.aspose.email/EmailClient#bindIPEndPoint\(com.aspose.email.BindIPEndPointHandler\)) property.

The API's [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient) can be set to use a specific IP address on the host by specifying the specific IP Endpoint. The following code sample can be used to achieve this.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-smtp-BindSMTPClientToSpecificIPAddressOnHost-.java" >}}
