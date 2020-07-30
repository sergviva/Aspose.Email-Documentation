---
title: Installation
type: docs
weight: 50
url: /java/installation/
---

## **Installing Aspose.Email for Java from Maven Repository**
Aspose hosts all Java APIs on [Aspose Artifactory](https://repository.aspose.com/webapp/#/home). You can easily use [Aspose.Email for Java](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-email) API directly in your Maven Projects with simple configurations.
### **Specify Maven Repository Configuration**
First, you need to specify the Aspose Maven Repository configuration/location in your Maven pom.xml as follows:

{{< highlight java >}}

 <repositories>

    <repository>

        <id>AsposeJavaAPI</id>

        <name>Aspose Java API</name>

        <url>http://repository.aspose.com/repo/</url>

    </repository>

</repositories>

{{< /highlight >}}
### **Define Aspose.Email for Java API Dependency**
Then define Aspose.Email for Java API dependency in your pom.xml as follows:

{{< highlight java >}}

 <dependencies>

    <dependency>

        <groupId>com.aspose</groupId>

        <artifactId>aspose-email</artifactId>

        <version>19.12</version>

        <classifier>jdk16</classifier>

 </dependency>

</dependencies>

{{< /highlight >}}

After performing the above steps, Aspose.Email for Java dependency will finally be defined in your Maven Project.
