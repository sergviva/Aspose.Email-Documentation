---
title: Gmail Utility Features
type: docs
weight: 10
url: /net/gmail-utility-features/
---


## **Working with FreeBusy Query**
Aspose.Email provides querying mechanism to check whether some appointment is due or not as per the criteria. FreebusyQuery class is provided for this purpose which allows to prepare a query for a particular calendar.
### **Querying a calendar**
This code sample demonstrates the feature of querying a calendar. Following tasks are performed in this sample:

1. Create and insert a calendar
1. Create an appointment
1. Insert appointment
1. Prepare a FreeBusyQuery
1. Get the FreebusyResponse



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-QueryingCalendar-QueryingCalendar.cs" >}}
## **Creating project in Google Developer Console**
A Project is to be created on Google Developer Console for a user having Gmail account. In the API & auth -> Credentials page of the Google project, information is to be noted like Client ID and Client Secret. This information along with the gmail account user name and password will be required for executing the code e.g. google calendar, access control lists, appointments, contacts, settings etc. in this section.
### **Steps to create a project in Google Developer Console**
Following is a step by step tutorial for creating a project in Google Developer Console.

\1. Go to link <https://cloud.google.com/console/project> and login using your gmail credentials

|![todo:image_alt_text](gmail-utility-features_1.png)|
| :- |
\2. Select the check box "I have read and agree to all Terms of Service for the Google Cloud Platform products." and Press Create button

|![todo:image_alt_text](gmail-utility-features_2.png)|
| :- |
\3. "SMS Verification" will be requested. Press continue button:

|![todo:image_alt_text](gmail-utility-features_3.png)|
| :- |
\4. Enter your country name and enter mobile number. Press button: Send Verification Code

|![todo:image_alt_text](gmail-utility-features_4.png)|
| :- |
\5. Enter the verification code received on your mobile.

|![todo:image_alt_text](gmail-utility-features_5.png)|
| :- |
\6. In the APIs & auth \ APIs list switch on status of Calendar API and Contacts API. Switch OFF all others.

|![todo:image_alt_text](gmail-utility-features_6.png)|
| :- |
\7. On the APIs & auth -> Credentials, press button "CREAET NEW CLIENT ID" under "OAuth" section. Select "Installed application" and "Other" from the given choices, and press the "Create Client ID" button. Note the Client ID and Client Secret here that will be used in the sample codes in this section.

|![todo:image_alt_text](gmail-utility-features_7.png)|
| :- |
## **Helper Classes**
Following helper classes are required to run the codes in this section. These classes GoogleOAuthHelper and GoogleTestUser are just for simplification of demonstration. The methods in these classes use non-public structure of web-pages that may change any time.
### **GoogleOAuthHelper Class**
The following code snippet shows you how to use GoogleOAuthHelper Class.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-GoogleOAuthHelper-GoogleOAuthHelper.cs" >}}
### **TestUser Class**
The following code snippet shows you how to use TestUser Class.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-TestUser-TestUser.cs" >}}
### **GoogleTestUser Class**
The following code snippet shows you how to use GoogleTestUser Class.



{{< gist "aspose-email" "9e8fbeb51a8cbc4129dc71ca8cd55f0b" "Examples-CSharp-Gmail-GoogleTestUser-GoogleTestUser.cs" >}}
