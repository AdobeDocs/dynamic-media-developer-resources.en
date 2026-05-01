---
description: This is the primary log which keeps track of all HTTP requests made to the [!DNL Platform Server]. Image Rendering, if enabled, writes its access log data to the same file.
solution: Experience Manager
title: Access log
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
TQID: https://experienceleague.adobe.com/S2ZKWZEX1eID19iKtN9MdmteAQca3UxX2DNPnf7Vxvg
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Access log{#access-log}

This is the primary log which keeps track of all HTTP requests made to the [!DNL Platform Server]. Image Rendering, if enabled, writes its access log data to the same file.

The access log is configured in server.xml.

>[!NOTE]
>
>In addition to client traffic for Image Serving ( [!DNL /is/image/*]) and Image Rendering ( [!DNL /ir/render/*]), the access log may include certain internal traffic: access to the [!DNL Platform Server] catalog system ( [!DNL /is-catalog/*]), cache sharing and error redirect requests ( [!DNL /is/cache/*]), access to other packages deployed to the [!DNL Platform Server], such as the Dynamic Media Viewers ( [!DNL /is-viewers/*]), static traffic and static contents requests serviced by the [!DNL Platform Server] (for example, [!DNL /is-docs/*]).

Requests with [!DNL /is-catalog] and [!DNL /is/cache] root paths should always be excluded from any client traffic analysis.
