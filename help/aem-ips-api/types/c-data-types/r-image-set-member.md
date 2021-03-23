---
description: Assets that belong to an image set.


solution: Experience Manager
title: ImageSetMember

feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Administrator
---

# ImageSetMember{#imagesetmember}

Assets that belong to an image set.

 Page reset means that an [!DNL eCatalog] should start a new page. `RenderSet` indicates that it is part of a `RenderSet` swatch. The value is forced to `true` for `eCatalog` and `RenderSet` sets. 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`asset`*`  | `type:Asset`  | Assets in the image set array.  |
|  `*`pageReset`*`  | `xsd:boolean`  |Starts a new page. Setting is ignored and value is forced to `true` for `eCatalog` and `RenderSet` sets.  |

