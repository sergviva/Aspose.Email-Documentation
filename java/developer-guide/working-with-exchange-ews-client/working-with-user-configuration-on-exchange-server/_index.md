---
title: Working with User Configuration on Exchange Server
type: docs
weight: 130
url: /java/working-with-user-configuration-on-exchange-server/
---

{{% alert color="primary" %}} 

Aspose.Email for Java can be used to manage user configuration on an Exchange Server with the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class. This class uses Exchange Web Services, which are only available in Exchange Server 2007 and later releases.

In this article, we will see how to read, create, update and delete user configurations on Exchange Server 2010.

{{% /alert %}} {{% alert color="primary" %}} 

Microsoft Exchange Server 2010 Service Pack 1 is required for all the features described in this article.

{{% /alert %}} 
## **Connect to an Exchange Server**
Below is the code used to connect to Exchange Server 2010 in all the examples in this article.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageRules-GetAsposeEWSClient.java" >}}
## **Read User Configuration**
To get the user configuration information of a specific folder from the Exchange Server:

1. Connect to Exchange Server using the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class.
1. Call the [IEWSClient.getUserConfiguration()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#getUserConfiguration\(com.aspose.email.UserConfigurationName\)) method to get the user configuration for a folder.
1. Display the user configuration properties like ID, name and dictionary items as key-value pairs.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageUserConfiguration-ReadUserConfiguration.java" >}}
## **Create User Configurations**
To create the user configuration for a specific folder on an Exchange Server:

1. Connect to the Exchange Server using the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class.
1. Call the [IEWSClient.createUserConfiguration()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#createUserConfiguration\(com.aspose.email.UserConfiguration\)) method to create the user configuration for a folder.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageUserConfiguration-CreateUserConfigurations.java" >}}
## **Update User Configuration**
To update the user configuration for a specific folder in the Exchange Server:

1. Connect to the Exchange Server using the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class.
1. Call the [IEWSClient.updateUserConfiguration()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#updateUserConfiguration\(com.aspose.email.UserConfiguration\)) method to update the user configuration for a folder.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageUserConfiguration-UpdateUserConfiguration.java" >}}
## **Delete User Configuration**
To delete the user configuration for a specific folder in the Exchange Server:

1. Connect to the Exchange Server using the [EWSClient](https://apireference.aspose.com/java/email/com.aspose.email/ewsclient) class.
1. Call the [IEWSClient.deleteUserConfiguration()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#deleteUserConfiguration\(com.aspose.email.UserConfigurationName\)) method to delete the user configuration for a folder.
 

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ManageUserConfiguration-DeleteUserConfiguration.java" >}}
