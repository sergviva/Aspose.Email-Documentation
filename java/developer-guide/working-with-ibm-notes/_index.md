---
title: Working with IBM Notes
type: docs
weight: 120
url: /java/working-with-ibm-notes/
---

## **About IBM Notes**
IBM Notes is the client and IBM Domino is the server of a collaborative client-server software platform. IBM Notes provides collaboration features like email, calendars, to-do lists, contacts management, etc. The database file used by IBM Notes is saved in the Notes Storage Facility (NSF) format.
## **Read messages from NSF storage file**
Aspose.Email provides the NotesStorageFacility class to read NSF storage files. The NotesStorageFacility class provides the EnumerateMessages method which iterates over the messages in the NSF storage file. The following sample code demonstrates the use of the NotesStorageFacility class and the EnumerateMessages method to read messages from the NSF storage file. 



{{< gist "aspose-com-gists" "709d733586ce50505c3bca3f6e8bd18d" "Examples-src-main-java-com-aspose-email-examples-email-ReadMessagesFromNSFStorage-1.java" >}}

{{% alert color="primary" %}} 

Please note that only message reading is implemented. Reading of folders is not supported yet due to lack of specification.

{{% /alert %}}
