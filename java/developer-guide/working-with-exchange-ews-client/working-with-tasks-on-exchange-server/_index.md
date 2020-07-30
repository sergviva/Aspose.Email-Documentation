---
title: Working with Tasks on Exchange Server
type: docs
weight: 120
url: /java/working-with-tasks-on-exchange-server/
---

{{% alert color="primary" %}} 

Aspose.Email supports processing tasks on Exchange using the [ExchangeTask](https://apireference.aspose.com/java/email/com.aspose.email/exchangetask) class. Different properties exposed by [ExchangeTask](https://apireference.aspose.com/java/email/com.aspose.email/exchangetask), like [Subject](https://apireference.aspose.com/java/email/com.aspose.email/Task#getSubject\(\)), [Status](https://apireference.aspose.com/java/email/com.aspose.email/ExchangeTask#getStatus\(\)), [DueDate](https://apireference.aspose.com/java/email/com.aspose.email/Task#getDueDate\(\)), and [Priority](https://apireference.aspose.com/java/email/com.aspose.email/Task#getPriority\(\)), can be used to configure the task on Exchange.

The [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class exposes functions like [CreateTask](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#createTask\(com.aspose.email.ExchangeTask\)), [UpdateTask](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#updateTask\(com.aspose.email.ExchangeTask\)), and [DeleteTask](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#deleteTask\(java.lang.String\)) which are used to process tasks on Exchange.

{{% /alert %}} 
## **Process Exchange Tasks**
The following examples show how to use the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class to retrieve tasks on Exchange.
### **Create a new Task on Exchange**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-Tasks-CreateNewTaskOnExchange.java" >}}
### **Specify Timezone for Exchange Task**
The [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) interface and [ExchangeTask](https://apireference.aspose.com/java/email/com.aspose.email/exchangetask) provide the TimeZoneId property for setting timezone information when creating a task.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-Tasks-SpecifyTimezoneForExchangeTask.java" >}}
### **Update Task on Exchange**
The following code snippets show how to update a task on an Exchange server.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-Tasks-UpdateTaskOnExchange.java" >}}
### **Delete Task on Exchange**
The code snippets below show how to delete a task on an Exchange server.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-Tasks-DeleteTaskOnExchange.java" >}}
## **Send Task Request**
Aspose.Email Exchange service provides the capability to send task requests similar to Outlook. The following code sample demonstrates how to load a task request message from the disc and send it using the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient).

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-Tasks-SendTaskRequest.java" >}}
## **Save Exchange Task to Disc**
Aspose.Email also allows saving Exchange Tasks to disc in Outlook MSG format.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-Tasks-SaveExchangeTaskToDisc.java" >}}
## **Listing Tasks from Exchange Server**
[IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) provides the [listTasks](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#listTasks\(\)) method that can be used to fetch tasks from an Exchange Web Service. It has several overloads that can be used to retrieve a list of tasks from a specific folder or using some search criteria. The below code sample illustrates getting all or specific tasks from the Tasks folder.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ListingTasksFromExchangeServerUsingEWS-ListTasksFromExchangeServerUsingEWS.java" >}}
## **Filtering Tasks from Mailbox**
Aspose.Email provides the capability to retrieve specific tasks from the server instead of retrieving all tasks from the server. The API can be used to retrieve tasks by task's status such as Completed, Deferred, In Progress, Not started or Waiting on others. The [ExchangeQueryBuilder](https://apireference.aspose.com/java/email/com.aspose.email/ExchangeQueryBuilder) class can be used to specify the desired criterion utilizing the [getTaskStatus()](https://apireference.aspose.com/java/email/com.aspose.email/ExchangeQueryBuilder#getTaskStatus\(\)) method. It also allows specifying multiple conditions for retrieving desired tasks from Exchange Server. This is demonstrated by the following code sample.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-Tasks-FilterTasksFromExchangeServer.java" >}}
