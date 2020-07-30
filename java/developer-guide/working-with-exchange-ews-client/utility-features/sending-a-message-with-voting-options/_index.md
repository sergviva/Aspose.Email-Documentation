---
title: Sending a Message with Voting Options
type: docs
weight: 60
url: /java/sending-a-message-with-voting-options/
---

{{% alert color="primary" %}} 

Microsoft Outlook allows users to create a poll when a new message is composed. This is done by including voting options such as Yes, No, Maybe, etc. The [FollowUpOptions](https://apireference.aspose.com/java/email/com.aspose.email/FollowUpOptions) class offered by Aspose.Email provides the [VotingButtons](https://apireference.aspose.com/java/email/com.aspose.email/FollowUpOptions#getVotingButtons\(\)) property that can be used to set or get the value of the voting options. This article provides a detailed example of creating a [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/mapimessage) with voting options for creating a poll and then sending the message using Exchange Web Service (EWS) client.

{{% /alert %}} 
## **Create and Send a Message with Voting Options**
The following code sample shows how to create a new message and then send it with voting options.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-SendAMessageWithVotingOptions-.java" >}}
