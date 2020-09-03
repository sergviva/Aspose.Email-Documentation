---
title: Utility Features - SMTP Client
type: docs
weight: 40
url: /java/utility-features-smtp-client/
---

## **Listing Extension Servers using Smtp Client**
Aspose.Email's SmtpClient lets you retrieve the server extensions that a server supports such as IDLE, UNSELECT, QUOTA, etc. This helps in identifying the availability of an extension before using the client for that particular functionality. The getCapabilities() method returns the supported extension types in the form of a string array.
### **Java**
{{< gist "" "e3443fa9baa07df6d929fc4a408add67" "Examples-src-main-java-com-aspose-email-examples-smtp-RetrieveServerExtensions-.java" >}}
## **Working with Signed Messages**
Aspose.Email API provides the capability to create Signed messages using certificates. The AttachSignature method can be used to sign a message for saving or even sending it using the SmtpClient.
### **Sign a Message**
**Java**

``` java

 String publicCertFile = @"sample.cer";

String privateCertFile = @"sample.pfx";

X509Certificate2 publicCert = new X509Certificate2(publicCertFile);

X509Certificate2 privateCert = new X509Certificate2(privateCertFile, "password");

MailMessage msg = new MailMessage("userfrom@gmail.com", "userto@gmail.com", "Signed message only", "Test Body of signed message");

MailMessage signed = msg.attachSignature(privateCert);

MailMessage encrypted = signed.encrypt(publicCert);

MailMessage decrypted = encrypted.decrypt(privateCert);

MailMessage unsigned = decrypted.removeSignature();//The original message with proper body

MapiMessage mapi = MapiMessage.fromMailMessage(unsigned);

```
### **Using Detached Signature Option**
**Java**

``` java

 String privateCertFile = "38445.pfx";

X509Certificate2 privateCert = new X509Certificate2(privateCertFile, "3p8a4s4s5word");

MailMessage msg = new MailMessage("dr38445@gmail.com", "dr38445@gmail.com", "subject:Signed message only by AE", "body:Test Body of signed message by AE");

MailMessage signed = msg.attachSignature(privateCert, true);

SmtpClient smtp = getSmtpClient(); //some test smtp client

smtp.send(signed);

```
## **Sign Emails with DKIM**
Aspose.Email allows to sign Email with DKIM (DomainKeys Identified Mail). This lets an organization take responsibility for a message that is in transit ([More Info](http://www.dkim.org)). DKIM adds a digital signature to the email message headers that can be validated by recipients. The public key of sender enables the receiver to verify that the signature matches the message's contents. The MailMessage class's DKIMSign method is used to set the cryptographic and signature information for signing the message.

The following code sample illustrates the process of signing an email with DKIM. The file key2.pem represents user's private key.

**Java**

``` java

 String Host= "smtp.domain.com", UserName ="Sender@domain.com", Password = "password";

int Port = 587;

String privateKeyFile = "key2.pem";

RSACryptoServiceProvider rsa = PemReader.getPrivateKey(privateKeyFile);

DKIMSignatureInfo signInfo = new DKIMSignatureInfo("test", "yandex.ru");

signInfo.getHeaders().addItem("From");

signInfo.getHeaders().addItem("Subject");

MailMessage mailMessage = new MailMessage("from@domain.com", "test@gmail.com");

mailMessage.setSubject("Signed DKIM message text body");

mailMessage.setBody("This is a text body signed DKIM message");

MailMessage signedMsg = mailMessage.dKIMSign(rsa, signInfo);

try

{

    final SmtpClient client = new SmtpClient(Host, Port, UserName, Password);

    try /*JAVA: was using*/

    {

        client.send(signedMsg);

    }

    finally { if (client != null) ((IDisposable)client).dispose(); }

}

finally

{

}

```
