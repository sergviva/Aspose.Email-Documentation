---
title: Setting Follow Up Flag and Due Date for Outlook Message (MSG) Files
type: docs
weight: 50
url: /java/setting-follow-up-flag-and-due-date-for-outlook-message-msg-files/
---

{{% alert color="primary" %}} 

A follow-up flag marks an email message for some kind of action. Microsoft Outlook lets users flag messages and, in the flag set-up, assign a due date for the follow-up. Microsoft Outlook sends a reminder to the recipient to prompt them to follow up on the email. Flagging emails and setting due dates programmatically lets software developers automate certain types of emails and help recipients remember to take action. For example, it could be used to send monthly messages to a sales team to remind them to complete their reports; or to send a message to all staff to remind them of a company meeting.

Aspose.Email for Java supports setting follow up flags and due dates for the [MapiMessage](https://apireference.aspose.com/java/email/com.aspose.email/MapiMessage) objects using [FollowUpManager](https://apireference.aspose.com/java/email/com.aspose.email/FollowUpManager) and [FollowUpOptions](https://apireference.aspose.com/java/email/com.aspose.email/FollowUpOptions).

{{% /alert %}} 
## **Set Flags and Due Dates**
There are a number of variants in which the follow-up flag can be set on a message. They are all used in the code sample below:

1. Set a follow-up flag for a message.
1. Add a due date and reminder date to a message.
1. Add a flag to a recipient's message.
1. Mark as complete.
1. Remove flag.
1. Read follow up options.
### **Set a FollowUp flag**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-SetFollowUpFlagAndDueDateForOutlookMessageFile-SettingAFollowUpFlag.java" >}}




|![todo:image_alt_text](http://i.imgur.com/hamEUFV.png)|
| :- |
### **Set Follow Up for Recipients**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-SetFollowUpFlagAndDueDateForOutlookMessageFile-SettingFollowUpForRecipients.java" >}}

|![todo:image_alt_text](http://i.imgur.com/Ip5Pq2a.png)|
| :- |
### **Mark a FollowUp flag as Completed**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-SetFollowUpFlagAndDueDateForOutlookMessageFile-MarkingAFollowUpFlagAsCompleted.java" >}}



![todo:image_alt_text](http://i.imgur.com/V5Q7CNW.png)
### **Remove a FollowUp flag**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-SetFollowUpFlagAndDueDateForOutlookMessageFile-RemovingAFollowUpFlag.java" >}}
### **Read followup flag options for a message**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-outlook-msg-SetFollowUpFlagAndDueDateForOutlookMessageFile-ReadFollowUpFlagOptionsForAMessage.java" >}}
