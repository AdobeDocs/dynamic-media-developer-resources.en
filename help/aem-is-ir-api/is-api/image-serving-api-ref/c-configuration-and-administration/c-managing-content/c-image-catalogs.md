---
description: Image catalogs provide many server configuration settings, as well as fonts, ICC profiles, command macros.
solution: Experience Manager
title: Image catalogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
TQID: 'https://experienceleague.adobe.com/kfojwk0K5RfRtZdxJmdojqsLirnP6LoXbtFRJ5272lg'
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
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Image catalogs{#image-catalogs}

Image catalogs provide many server configuration settings, as well as fonts, ICC profiles, command macros.

They map image and static content ids used in requests to actual file paths, store various image metadata, such as image maps, and provide containers for templates and image sets.

Image catalogs are accessed only by the [!DNL Platform Server], never by the Image Server. Catalog attribute files must have an .ini suffix and be placed in the [!DNL Platform Server]'s catalog folder ( `PS::CatalogFolder`). At least the default image catalog is required and must be populated with all attributes for correct functioning of the [!DNL Platform Server].
