---
title: Download Messages from Exchange Server Folders and Subfolders Recursively
type: docs
weight: 20
url: /java/download-messages-from-exchange-server-folders-and-subfolders-recursively/
---

{{% alert color="primary" %}} 

The EWSClient’s [listSubFolders()](https://apireference.aspose.com/java/email/com.aspose.email/IEWSClient#listSubFolders\(com.aspose.email.ExchangeFolderInfo\)) method can be used to get messages from folders and subfolders from an Exchange Server mailbox recursively. This requires Exchange Server 2007 or greater because it uses EWS.

{{% /alert %}} 

The example below shows how to download the whole mailbox (folders and subfolders) of an Exchange Server. The folder structure is created locally and all messages download.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-exchange-DownloadMessagesFromAnExchangeServerFoldersRecursively-.java" >}}
