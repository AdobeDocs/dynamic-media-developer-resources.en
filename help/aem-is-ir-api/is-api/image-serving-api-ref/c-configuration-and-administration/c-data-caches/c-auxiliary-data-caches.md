---
description: Intermediate image data produced by nested/embedded Image Serving and Image Rendering requests can be cached by specifying cache=on in the nested/embedded request. This data is stored in proprietary format in the response data cache.
solution: Experience Manager
title: Auxiliary data caches
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
TQID: https://experienceleague.adobe.com/4bX0Sy16KhG15IEvL24nn1qvEpBBx5M4mLfIrcwqaVM
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
# Auxiliary data caches{#auxiliary-data-caches}

Intermediate image data produced by nested/embedded Image Serving and Image Rendering requests can be cached by specifying cache=on in the nested/embedded request. This data is stored in proprietary format in the response data cache.

Images obtained from foreign HTTP servers are also stored in the response data cache. Such images are validated automatically with the validate utility before the cache entry is generated.

The [!DNL Platform Server] compiles image catalog data for efficient access. This data is stored in `CS::CatalogCacheFolder`.
