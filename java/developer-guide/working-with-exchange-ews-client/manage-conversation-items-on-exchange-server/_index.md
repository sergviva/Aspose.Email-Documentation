---
title: Manage Conversation Items on Exchange Server
type: docs
weight: 50
url: /java/manage-conversation-items-on-exchange-server/
---

{{% alert color="primary" %}} 

Aspose.Email for Java can be used to manage the conversation items on Exchange Server with the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class. This class uses Exchange Web Services, which are only available in Exchange Server 2007 and later releases.

This article shows how to find, copy, update and delete conversation items on Exchange Server 2010.

{{% /alert %}} {{% alert color="primary" %}} 

Microsoft Exchange Server 2010 Service Pack 1 is required for all the features included in this section.

{{% /alert %}} 
## **Connect to an Exchange Server**
Below is the code uses to connect to Exchange Server 2010 in all the examples in this article.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageRules-GetAsposeEWSClient.java" >}}
## **Find Conversations**
To get the conversation information from a specific folder on the Exchange Server:

1. Connect to the Exchange Server using the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class.
1. Call the [IEWSClient.findConversations()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#findConversations\(java.lang.String\)) method to find all the conversation items from a folder.
1. Display the conversation item properties like ID, the conversation topic and flag status.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageConversationItems-FindConversations.java" >}}
## **Copy Conversations**
To copy conversations from one folder to another:

1. Connect to the Exchange Server using the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class.
1. Call the [IEWSClient.copyConversationItems()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#copyConversationItems\(java.lang.String,%20java.lang.String\)) method to copy the conversation item from the source folder to the destination folder.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageConversationItems-CopyConversations.java" >}}
## **Move Conversations**
To move conversations from one folder to another:

1. Connect to the Exchange Server using the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class.
1. Call the [IEWSClient.moveConversationItems()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#moveConversationItems\(java.lang.String,%20java.lang.String\)) method to move a conversation from the source folder to the destination folder.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageConversationItems-MoveConversations.java" >}}
## **Delete Conversations**
To delete conversations from a folder:

1. Connect to the Exchange Server using the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class.
1. Call the [IEWSClient.deleteConversationItems()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#deleteConversationItems\(java.lang.String\)) method to delete the conversation item from the source folder.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageConversationItems-DeleteConversations.java" >}}
