---
title: Fetching Messages and Saving to Disc
type: docs
weight: 60
url: /java/fetching-messages-and-saving-to-disc/
---

Aspose.Email's [ImapClient](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient) provides the capability to list messages from an IMAP server into [ImapMessageInfoColleciton](https://apireference.aspose.com/java/email/com.aspose.email/ImapMessageInfoCollection). The [ImapMessageInfo](https://apireference.aspose.com/java/email/com.aspose.email/ImapMessageInfo) provides summary information about the message to be retrieved such as subject, sent date, sender information, message id, and others. Information from [ImapMessageInfo](https://apireference.aspose.com/java/email/com.aspose.email/ImapMessageInfo) can be used to fetch messages from the server into an instance of [MailMessage](https://apireference.aspose.com/java/email/com.aspose.email/MailMessage) which then allows to store it on disc in any desirable formats.
## **List Messages from Inbox of IMAP server**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FetchMessagesAndSaveToDisc-ListMessagesFromInboxOfIMAPServer.java" >}}
## **List Messages from a Folder**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FetchMessagesAndSaveToDisc-ListMessagesRecursivelyFromFolders.java" >}}
## **Get Messages in descending order**
Aspose.Email provides [ImapClient.ListMessagesByPage](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#listMessagesByPage\(int,%20com.aspose.email.PageSettings\)) method which lists messages with paging support.Some overloads of [ImapClient.ListMessagesByPage](https://apireference.aspose.com/java/email/com.aspose.email/ImapClient#listMessagesByPage\(int,%20com.aspose.email.PageSettings\)) accept [PageSettings](https://apireference.aspose.com/java/email/com.aspose.email/PageSettings) as a parameter. [PageSettings](https://apireference.aspose.com/java/email/com.aspose.email/PageSettings) provides an [AscendingSorting](https://apireference.aspose.com/java/email/com.aspose.email/PageSettings#setAscendingSorting\(boolean\)) property which when set to **false**, returns emails in descending order.

The following example code demonstrates the use of [AscendingSorting](https://apireference.aspose.com/java/email/com.aspose.email/PageSettings#setAscendingSorting\(boolean\)) property of the [PageSettings](https://apireference.aspose.com/java/email/com.aspose.email/PageSettings) class to change the order of emails.

{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-ChangeOrderOfEmails-1.java" >}}
## **Fetch Messages By Sequence Number and Save to Disc**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FetchMessagesAndSaveToDisc-FetchMessagesBySequenceNumber.java" >}}
## **Fetch Messages By Message Id and Save to Disc**
{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-imap-FetchMessagesAndSaveToDisc-FetchMessagesByMessageId.java" >}}
## **Retrieve "N" number of Messages from Server**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-imap-FetchMessagesAndSaveToDisc-RetrieveNNumberOfMessagesFromServer.java" >}}
## **Retrieve Extra Parameters as Summary Information**


``` java

 ImapClient client = new ImapClient("host.domain.com", "username", "password");

{

    try

    {

        MailMessage message = new MailMessage(

                "from@domain.com",

                "to@doman.com",

                "EMAILNET-38466 - Retrieve Extra Parameters as Summary Info." ,

                "EMAILNET-38466 Add extra parameters for UID FETCH command");

        //append the message to the server

        String uid = client.appendMessage(message);

        //wait for the message to be appended

        Thread.sleep(5000);

        //Define properties to be fetched from server along with the message

        List<String> messageExtraFields = new List<String>();

        messageExtraFields.add("X-GM-MSGID");

        messageExtraFields.add("X-GM-THRID");

        //retreive the message summary information using it's UID

        ImapMessageInfo messageInfoUID = client.listMessage(uid, messageExtraFields);

        //retreive the message summary information using it's sequence number

        ImapMessageInfo messageInfoSeqNum = client.listMessage(1, messageExtraFields);

        //List messages in general from the server based on the defined properties

        ImapMessageInfoCollection messageInfoCol = client.listMessages(messageExtraFields);

        ImapMessageInfo messageInfoFromList = messageInfoCol.get_Item(0);

        //verify that the parameters are fetched in the summary information

        for (String paramName:messageExtraFields)

        {

            System.out.println(messageInfoFromList.getExtraParameters().containsKey(paramName));

            System.out.println(messageInfoUID.getExtraParameters().containsKey(paramName));

            System.out.println(messageInfoSeqNum.getExtraParameters().containsKey(paramName));

        }

    }

    finally

    {

    }

}

```
