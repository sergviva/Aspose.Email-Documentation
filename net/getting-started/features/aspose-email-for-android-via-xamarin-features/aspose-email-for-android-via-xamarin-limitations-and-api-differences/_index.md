---
title: Aspose.Email for Android via Xamarin Limitations and API Differences
type: docs
weight: 10
url: /net/aspose-email-for-android-via-xamarin-limitations-and-api-differences/
---


Aspose.Email for Android via Xamarin has some limitations as compared to the Standard Aspose.Email for .NET API. These are as detailed below.
## **Latest Version of Aspose.Email for Android via Xamarin may not Work with Old Xamarin.Android Version**
Please note that Aspose.Email for Android via Xamarin is always built by using the latest stable versions of Xamarin and Xamarin.Android platforms. If you face any problems when using Aspose.Email for Android via Xamarin in your Xamarin.Android application, please make sure you have the latest Xamarin and Xamarin.Android versions installed. Sometimes Aspose.Email for Android via Xamarin built by using the latest Xamarin (Xamarin.Android) version does not work with older versions of Xamarin.
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
1. All Aspose.Email methods taking System.Stream as a parameter require the stream to be seekable and has a length. This may not be the case for some Xamarin Streams. For example, Android Assets and raw Resources are available as streams, but if one will pass such a stream to the Aspose.Email API, it will result in NotSupportedException.
## **Work Around Method for Working with Xamarin Streams**
The following code sample illustrates a work around method for loading Android Assets and raw Resources from stream.

``` java

 static class Tools

{

    internal static MemoryStream ReadAsset(String name)

    {

        using(var stream = global::Android.App.Application.Context.Assets.Open(name))

        {

            var res = new MemoryStream();

            stream.CopyTo(res);

            res.Position = 0;

            return res;

        }

    }

}

```
## **Usage Example**
``` java

 var stream = Tools.ReadAsset(@"Bounce/new 3.msg");

MapiMessage msg = MapiMessage.FromStream(stream);

```

