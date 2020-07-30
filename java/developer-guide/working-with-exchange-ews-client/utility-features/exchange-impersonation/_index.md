---
title: Exchange Impersonation
type: docs
weight: 40
url: /java/exchange-impersonation/
---

{{% alert color="primary" %}} 

Exchange impersonation allows someone to impersonate another account and perform tasks and operations using the impersonated account's permissions instead of their own. Where delegation lets users act **on behalf** of other users, Impersonation allows them to act **as** other users.
Aspose.Email supports Exchange Impersonation. The [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) interface provides the [ImpersonateUser](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#impersonateUser\(int,%20java.lang.String\)) and [ResetImpersonation](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#resetImpersonation\(\)) methods to facilitate this feature.

{{% /alert %}} 

The following example shows how to use the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) to implement the Impersonation feature.

To perform this task:

1. Initialize the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) for user 1.
1. Initialize the [IEWSClient](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient) for user 2.
1. Append test messages to the accounts.
1. Enable Impersonation.
1. Reset Impersonation.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-ExchangeImpersonation-.java" >}}
