---
title: Get messages from a shared mailbox
type: docs
weight: 190
url: /java/get-messages-from-a-shared-mailbox/
---

Aspose.Email supports accessing messages from the shared mailbox. To achieve this, you connect to your primary mailbox by using the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/EWSClient) class. To access messages from the shared mailbox, you pass the shared mailbox as a string parameter to the [ListMessages](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#listMessages\(java.lang.String,%20java.lang.String,%20boolean\)) or [ListItems](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#listItems\(java.lang.String,%20java.lang.String\)) method.

The following code sample shows how to access messages from the shared mailbox using the [ListItems](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#listItems\(java.lang.String,%20java.lang.String\)) method.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchangeews-GetMessagesFromSharedMailbox-1.java" >}}
