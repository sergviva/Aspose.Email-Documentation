---
title: Sending Tasks Requests
type: docs
weight: 30
url: /java/sending-tasks-requests/
---

Aspose.Email API allows manipulating Outlook Tasks for functions such as creating, saving and reading. In addition, the API allows sending Tasks Requests using the [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient). This article shows how to send a Task request using Aspose.Email for Java using its [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient).

Aspose.Email sends tasks requests by specifying these as TNEF special messages. Thus, the [MsgLoadOptionsclass](https://apireference.aspose.com/java/email/com.aspose.email/MsgLoadOptions) class is used to load such a Task MSG for sending using [SmtpClient](https://apireference.aspose.com/java/email/com.aspose.email/SmtpClient).

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-smtp-SendTasksRequests-.java" >}}
