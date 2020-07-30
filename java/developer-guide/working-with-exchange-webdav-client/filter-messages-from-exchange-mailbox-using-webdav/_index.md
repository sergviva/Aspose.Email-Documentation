---
title: Filter Messages from Exchange Mailbox using WebDav
type: docs
weight: 40
url: /java/filter-messages-from-exchange-mailbox-using-webdav/
---

{{% alert color="primary" %}} 

The [ExchangeClient](http://www.aspose.com/api/java/email/com.aspose.email/classes/ExchangeClient) class provides the listMessages() method which gets all messages from a mailbox. To get only messages which match some condition, use the overloaded listMessages() method which takes the [MailQuery](http://www.aspose.com/api/java/email/com.aspose.email/classes/MailQuery) class as an argument. The [MailQuery](http://www.aspose.com/api/java/email/com.aspose.email/classes/MailQuery) class provides various properties for specifying conditions, for example date, subject, sender and recipient. In addition, the API also allows to apply case-sensitivity filters for retrieving emails from mailbox.

{{% /alert %}} 
## **Filter Messages using Web Dav**
To get filtered messages from a mailbox:

1. Connect to Exchange server.
1. Create an instance of [MailQuery](http://www.aspose.com/api/java/email/com.aspose.email/classes/MailQuery) and set the desired properties.
1. Call the [ExchangeClient](http://www.aspose.com/api/java/email/com.aspose.email/classes/ExchangeClient).listMessages(MailQuery query) method and pass the MailQuery in the parameters to get the filtered messages only.

The code examples below show how to connect to an Exchange mailbox and get messages that have the string "Newsletter" in the subject and were sent today.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FilterMessagesFromExchangeMailbox-FilterMessages.java" >}}
## **Get Messages that Meet Specific Criteria**
The code samples above filters messages based on the email subject and date. We can filter on other properties too. Below are some examples of setting the conditions using [MailQuery](http://www.aspose.com/api/java/email/com.aspose.email/classes/MailQuery).
### **Code Samples: Today's Date**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FilterMessagesFromExchangeMailbox-FilterMessagesBasedOnTodayDate.java" >}}
#### **Code Samples: Date Range**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FilterMessagesFromExchangeMailbox-FilterMessagesBasedOnDateRange.java" >}}
#### **Code Samples: Specific Sender**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FilterMessagesFromExchangeMailbox-FilterMessagesBasedOnSpecificSender.java" >}}
#### **Code Samples: Specific Domain**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FilterMessagesFromExchangeMailbox-FilterMessagesBasedOnSpecificDomain.java" >}}
#### **Code Samples: Specific Recipient**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FilterMessagesFromExchangeMailbox-FilterMessagesBasedOnSpecificRecipient.java" >}}
#### **Code Samples: By MessageID**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FilterMessagesFromExchangeMailbox-FilterMessagesBasedOnMessageID.java" >}}
## **Building Complex Queries**
If different QueryBuilder properties are set in separate statement, all the conditions are matched. For example,to get a message in a particular date range and from a specific host, write three statements:
### **Code Samples: Combining Queries with AND**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FilterMessagesFromExchangeMailbox-CombineQueriesWithAND.java" >}}
### **Code Samples: Combining Queries with OR**
QueryBuilder provides the Or() method which takes two MailQuery instances as parameters. It gets messages that match any of the two conditions specified. The example below filters messages that either has the word “test” in the subject or “noreply@host.com” as the sender.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FilterMessagesFromExchangeMailbox-CombiningQueriesWithOR.java" >}}
## **Case-Sensitive Email Filtering**
Emails can be filtered based on case-sensitivity by specifying the IgnoreCase flag in the filter criteria as shown in the following example.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-FilterMessagesFromExchangeMailbox-FilterMessagesBasedCaseSensitivity.java" >}}
