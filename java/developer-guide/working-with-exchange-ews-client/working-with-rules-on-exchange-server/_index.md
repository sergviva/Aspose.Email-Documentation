---
title: Working with Rules on Exchange Server
type: docs
weight: 110
url: /java/working-with-rules-on-exchange-server/
---

Aspose.Email for Java can be used to manage the rules on Exchange Server using the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/EWSClient) class. This class uses Exchange Web Services (EWS), which are available in Exchange Server 2007 and later releases.

{{% alert color="primary" %}} 

Microsoft Exchange Server 2010 Service Pack 1 is required for all features described in this article.

{{% /alert %}} 
## **Connect to an Exchange Server**
Below is the code that uses to connect to Exchange Server 2010 in all the examples used in this article.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageRules-GetAsposeEWSClient.java" >}}
## **Read the Rules**
To get all the rules from the Exchange Server:

1. Connect to an Exchange Server using the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) class.
1. Call the [IEWSClient.getInboxRules()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#getInboxRules\(\)) method to get all the rules.
1. In a for each loop, browse through all the rules and display the rule properties like conditions, actions, and names.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageRules-ReadRules.java" >}}
## **Create a New Rule**
To create a new rule on the Exchange Server, perform the following steps:

1. Connect to an Exchange Server using the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) class.
1. Create a new instance of the [InboxRule](https://apireference.aspose.com/java/email/com.aspose.email/inboxrule) class and set the following mandatory properties:
   1. [DisplayName](https://apireference.aspose.com/java/email/com.aspose.email/InboxRule#setDisplayName\(java.lang.String\))
   1. [Conditions](https://apireference.aspose.com/java/email/com.aspose.email/InboxRule#setConditions\(com.aspose.email.RulePredicates\))
   1. [Actions](https://apireference.aspose.com/java/email/com.aspose.email/InboxRule#setActions\(com.aspose.email.RuleActions\))
1. Call the [IEWSClient.createInboxRule()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#createInboxRule\(com.aspose.email.InboxRule\)) method to create the rule.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageRules-CreateANewRule.java" >}}
## **Update an existing rule**
To update a rule on the Exchange Server:

1. Connect to an Exchange Server using the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) class.
1. Call the [IEWSClient.getInboxRules()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#getInboxRules\(\)) method to get all the rules.
1. In a for each loop, browse through all the rules and get the rule you want to change by matching the [DisplayName](https://apireference.aspose.com/java/email/com.aspose.email/InboxRule#getDisplayName\(\)) in a condition.
1. Update the rule properties
1. Call the [IEWSClient.updateInboxRule()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#updateInboxRule\(com.aspose.email.InboxRule\)) method to update the rule.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageRules-UpdateARule.java" >}}
