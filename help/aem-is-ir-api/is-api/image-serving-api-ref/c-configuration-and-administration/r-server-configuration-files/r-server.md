---
description: Contains platform server settings.
seo-description: Contains platform server settings.
seo-title: server.xml
solution: Experience Manager
title: server.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
index: y
internal: n
snippet: y
---

# server.xml{#server-xml}

Contains platform server settings.

When modifying this XML file, care must be taken to maintain valid XML syntax, otherwise the Platform Server may fail to start.

For changes to take effect, the Platform Server must be restarted after editing this file.

The following diagram illustrates which settings may be changed in this file. Refer to the corresponding sections earlier in this document for a description of these settings. Note that this diagram is not a complete representation of [!DNL server.xml].

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```

