---
title: Access SMTP and IMAP Server using OAuth
type: docs
weight: 190
url: /net/access-smtp-and-imap-server-using-oauth/
---


Aspose.Email for .NET can be used to access SMTP and IMAP servers. OAuth support for Google mail is implemented only for version 2.0 as OAuth 1.0 has been [officially deprecated as of April 20, 2012](https://developers.google.com/accounts/docs/RegistrationForWebAppsAuto). At this moment, Google supports OAuth only for [the Google Apps Platform](https://developers.google.com/google-apps/gmail/oauth_overview) and public mail accounts can't be used with the OAuth mechanism. When a new Google Apps account is created, a new "Installed Application" should be registered for this account for testing in the APIs Console. [Free trial accounts](https://www.google.com/a/signup/?hl=en&source=gafb-homepage-canvas-en) can be created, provided by Google Apps for Business.
## **Using Aspose.Email to Access SMTP and IMAP Servers**
With Aspose.Email for .NET, it is possible to access SMTP and IMAP servers using OAuth. The following code snippet uses this feature to access SMTP and IMAP server.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Knowledge-Base-AccessSMTPAndIMAPServersUsingOAuth-AccessSMTPAndIMAPServersUsingOAuth.cs" >}}
