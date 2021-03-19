---
description: This is the primary log which keeps track of all HTTP requests made to the Platform Server. Image Rendering, if enabled, writes its access log data to the same file.
seo-description: This is the primary log which keeps track of all HTTP requests made to the Platform Server. Image Rendering, if enabled, writes its access log data to the same file.
seo-title: Access log
solution: Experience Manager
title: Access log
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Access log{#access-log}

This is the primary log which keeps track of all HTTP requests made to the Platform Server. Image Rendering, if enabled, writes its access log data to the same file.

The access log is configured in server.xml.

>[!NOTE]
>
>In addition to client traffic for Image Serving ( [!DNL /is/image/*]) and Image Rendering ( [!DNL /ir/render/*]), the access log may include certain internal traffic: access to the Platform Server catalog system ( [!DNL /is-catalog/*]), cache sharing and error redirect requests ( [!DNL /is/cache/*]), access to other packages deployed to the Platform Server, such as the Dynamic Media Viewers ( [!DNL /is-viewers/*]), static traffic and static contents requests serviced by the Platform Server (e.g. [!DNL /is-docs/*]).

Requests with [!DNL /is-catalog] and [!DNL /is/cache] root paths should always be excluded from any client traffic analysis. 
