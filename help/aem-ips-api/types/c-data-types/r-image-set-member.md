---
description: Assets that belong to an image set.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
TQID: 'https://experienceleague.adobe.com/53rc6Cq1i15GdzOpBek7ls7ixq4RN8z0OfZMOZsqYWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL ImageSetMember]{#imagesetmember}

Assets that belong to an image set.

 Page reset means that an [!DNL eCatalog] should start a new page. `RenderSet` indicates that it is part of a `RenderSet` swatch. The value is forced to `true` for `eCatalog` and `RenderSet` sets. 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  asset  | `type:Asset`  | Assets in the image set array.  |
|  pageReset  | `xsd:boolean`  |Starts a new page. Setting is ignored and value is forced to `true` for `eCatalog` and `RenderSet` sets.  |
