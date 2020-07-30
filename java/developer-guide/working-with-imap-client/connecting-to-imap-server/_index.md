---
title: Connecting to IMAP Server
type: docs
weight: 10
url: /java/connecting-to-imap-server/
---

The [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class allows applications to manage IMAP mailboxes using the IMAP protocol. The [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class is used to connect to IMAP mail servers and manage emails in the IMAP email folders.

The [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class allows connecting to any type of IMAP server. It can be used to connect to Non-SSL as well as SSL enabled IMAP servers.
## **Connect to IMAP Server**
In order to connect to an IMAP server, you need to create an instance of the [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class, specify the host name, user name and password as shown in the following code sample.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ConnectingToIMAPServer-ConnectingToIMAPServer.java" >}}
## **Connect to an SSL-Enabled IMAP server**
In order to connect to an SSL-enabled IMAP server, options from the [SecurityOptions](https://apireference.aspose.com/java/email/com.aspose.email/EmailClient#setSecurityOptions\(int\)) class can be specified as required. This is shown in the following code sample by connecting to Gmail server.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ConnectingToIMAPServer-ConnectingToAnSSLEnabledIMAPServer.java" >}}
## **Connect to Server using HTTP Proxy**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ConnectingToIMAPServer-AccessMailboxViaHttpProxy.java" >}}
## **Connecting to Server in Read-Only mode**
The [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) class provides a [ReadOnly](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#setReadOnly\(boolean\)) property which when set to **true**, indicates that no changes should be made to the permanent state of the mailbox. The following code sample demonstrates the use of [ImapClient.ReadOnly](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#setReadOnly\(boolean\)) property. It gets the count of unread messages, then fetches one message and then gets the count of unread messages again in read-only mode. The count of the unread messages remains the same indicating that the permanent state of the mailbox was not changed.



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ImapReadOnlyMode-1.java" >}}
