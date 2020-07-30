---
title: Utility Features
type: docs
weight: 140
url: /java/utility-features/
---

## **Auto Discover Feature using EWS**
Aspose.Email API lets you discover about the Exchange Server settings using the EWS Client.

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchangeews-AutoDiscoverUsingEWS-AutoDiscoverUsingEWS.java" >}}
## **Aborting PST to Exchange Server Operation**
Aspose.Email API lets you restore a PST file to Exchange Server. However, if the operation is taking long due to large size PST file, it may be required to specify criterion for aborting the operation. This can be achieved using the API as shown in the following sample code.

**Note:** The example needs the following class to be added as well.

{{< highlight java >}}

 public class AbortRestoreException : Exception { }

{{< /highlight >}}

{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-exchangeews-AbortPSTToExchangeServerOperation-AbortPSTToExchangeServerOperation.java" >}}
