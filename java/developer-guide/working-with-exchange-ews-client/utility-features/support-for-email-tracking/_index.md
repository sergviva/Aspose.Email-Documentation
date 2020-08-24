---
title: Support for Email Tracking
type: docs
weight: 70
url: /java/support-for-email-tracking/
---

{{% alert color="primary" %}} 

Aspose.Email API provides support of email tracking using Message Disposition Notification (MDN). This is achieved by requesting the read receipts and creating the required information. The MailMessage class’s ReadReceiptTo property gets or sets the set read receipt address. The CreateReadReceipt and ReadReceiptRequested methods are used for creating and retrieving the information whether read receipts are requested.

{{% /alert %}} 
## **Email Tracking**
The following code sample illustrates the example of email tracking using Aspose.Email API.

**Java**

``` java

 // Send message with the requested read receipt

{

    MailMessage eml = new MailMessage(fromAddress, toAddress, "test MDN",

        "This is a test message with read receipt requested");

    // request the read receipt

    eml.setReadReceiptTo(fromAddress);

    sendMessage(eml, SendMethod.SMTP);

}

// Add multiple ReadReceiptTo addresses. Send message with the requested read receipt.

{

    MailMessage eml = new MailMessage(fromAddress, toAddress, "test MDN",

        "This is a test message with read receipt requested");

    MailAddressCollection addressCollection = new MailAddressCollection();

    addressCollection.addItem(fromAddress);

    addressCollection.addItem(anotherAddress);

    // request the read receipt

    eml.setReadReceiptTo(addressCollection);

    sendMessage(eml, SendMethod.SMTP);

}

// Send message by Exchange

{

    MailMessage eml = new MailMessage(fromAddress, toAddress, "test MDN",

        "This is a test message with read receipt requested");

    // request the read receipt

    eml.setReadReceiptTo(fromAddress);

    sendMessage(eml, SendMethod.Exchange);

}

// Check the request, create and send read receipt.

{

    MailMessage emlMDN = fetchMessage();

    if (emlMDN.getReadReceiptTo().getSize() > 0)

    {

        sendMessage(emlMDN.createReadReceipt(toAddress, null), SendMethod.SMTP);

    }

}

// Create the MapiMessage with requested read receipt

{

    MapiMessage msg = new MapiMessage(fromAddress, toAddress, "test MDN", "This is a read requested msg", OutlookMessageFormat.Unicode);

    msg.setReadReceiptRequested(true);

}

// Create the MailMessage with requested read receipt and convert it to MapiMessage

{

    MailMessage eml = new MailMessage(fromAddress, toAddress, "test MDN",

        "This is a test message with read receipt requested");

    // request the read receipt

    eml.setReadReceiptTo(fromAddress);

    MapiMessage msg = MapiMessage.fromMailMessage(eml, MapiConversionOptions.UnicodeFormat);

}

// Create the MapiMessage with requested read receipt and convert it to MailMessage

{

    MapiMessage msg = new MapiMessage("dmitry.samodurov@aspose.com", "dmitry.samodurov@aspose.com", "test MDN", "This is a read requested msg", OutlookMessageFormat.Unicode);

    msg.setReadReceiptRequested(true);

    MailMessage mi = MailMessageInterpretorFactory.getInstance().getIntepretor(msg.getMessageClass());

    MailMessage mailMessage = mi.interpret(msg);

}

```
