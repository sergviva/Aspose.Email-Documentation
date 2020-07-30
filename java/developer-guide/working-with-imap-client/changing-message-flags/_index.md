---
title: Changing Message Flags
type: docs
weight: 70
url: /java/changing-message-flags/
---

The [changeMessageFlags](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#changeMessageFlags\(com.aspose.email.IConnection,%20int,%20com.aspose.email.ImapMessageFlags\)) method of [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) allows changing message flags. The method takes 2 parameters:

1. Message's Sequence Number or Unique Id
1. Message flag

The following flags can be set:

- Answered
- Deleted
- Draft
- Empty
- Flagged
- IsRead
- Read
- Recent
## **Set Message Flags**
The code examples below show how to change message flags on an IMAP server with Aspose.Email.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ChangeMessageFlags-SetMessageFlags.java" >}}
## **Remove Message Flags**
Message flags can also be removed with the [removeMessageFlags](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#removeMessageFlags\(com.aspose.email.IConnection,%20int,%20com.aspose.email.ImapMessageFlags\)) method. Usage is similar to that of the [changeMessageFlags](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#changeMessageFlags\(com.aspose.email.IConnection,%20int,%20com.aspose.email.ImapMessageFlags\)) method. It takes a sequence number or unique message ID and MessageFlag.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ChangeMessageFlags-RemovingMessageFlags.java" >}}
## **Setting Custom Flags**
You can also set custom flags to a message using the ImapClient of the API. The ImapClient's addMessageFlags provides the ability to set custom flags on messages.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-SetCustomFlag-SetCustomFlag.java" >}}
