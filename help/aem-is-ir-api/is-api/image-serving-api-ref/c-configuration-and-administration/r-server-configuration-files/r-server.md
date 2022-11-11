---
description: Contains platform server settings.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
---
# server.xml{#server-xml}

Contains platform server settings.

When modifying this XML file, care must be taken to maintain valid XML syntax, otherwise the [!DNL Platform Server] may fail to start.

For changes to take effect, the [!DNL Platform Server] must be restarted after editing this file.

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
