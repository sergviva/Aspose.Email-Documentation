---
title: Aspose.Email for iOS via Xamarin Limitations and API Differences
type: docs
weight: 10
url: /net/aspose-email-for-ios-via-xamarin-limitations-and-api-differences/
---


Aspose.Email for iOS via Xamarin has some limitations as compared to the Standard Aspose.Email for .NET API. These are as detailed below.
## **Latest Version of Aspose.Email for iOS via Xamarin may not Work with Old Xamarin.iOS Version**
Please note that Aspose.Email for iOS via Xamarin is always built by using the latest stable versions of Xamarin and iOS.Xamarin platforms. If you face any problems when using Aspose.Email for iOS via Xamarin in your Xamarin.iOS application, please make sure you have the latest Xamarin and Xamarin.iOS versions installed. Sometimes, Aspose.Email for iOS via Xamarin built by using the latest Xamarin (Xamarin.iOS) version does not work with older versions of Xamarin.
## **Missing Namespaces**
The API lacks the following namespaces.

|**Namespace**|**Impact**|
| :- | :- |
|Aspose.Email.Clients.ActiveSync.TransportLayer|Active Sync functionality will not be available|
|Aspose.Email.Windows|Android based applications don't require these as the functionality is related to Windows forms|
|Aspose.Email.Printing|Can't convert messages to XPS and TIFF formats|
## **Other Limitations**
1. You can not embed linked images into message body in both RTF as well as HTML format
1. It also has no functionality of Signing or Encrypting/Decrypting messages
