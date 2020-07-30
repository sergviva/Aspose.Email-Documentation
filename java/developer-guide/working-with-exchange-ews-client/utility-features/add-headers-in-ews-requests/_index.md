---
title: Add Headers in EWS Requests
type: docs
weight: 20
url: /java/add-headers-in-ews-requests/
---

{{% alert color="primary" %}} 

Aspose.Email API allows adding headers to Exchange requests. This can be used to add headers to the EWS requests for different headers that can be used for different purposes. Once such example could be adding the X-AnchorMailbox header that is used to manage the throttling issues on Exchange server.

{{% /alert %}} 

The addHeader() method of the IEWSClient is used to add headers to the EWS requests as shown in the following code sample.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchange-AddHeadersInEWSRequests-.java" >}}
