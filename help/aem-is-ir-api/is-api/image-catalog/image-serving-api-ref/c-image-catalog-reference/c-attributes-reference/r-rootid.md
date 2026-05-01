---
description: Catalog identifier. The HTTP path element used to identify this catalog in a request's image object specifier.
solution: Experience Manager
title: RootId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9224f06d-28a9-4a23-9a3a-735b2b9f87ff
TQID: https://experienceleague.adobe.com/2R2O5kLVGmo6wwm-pVU1-Fqa-TkZNdQ7088wjLRWswI
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# RootId{#rootid}

Catalog identifier. The HTTP path element used to identify this catalog in a request's image object specifier.

## Properties {#section-9a49da71de634378a06d2347790898a0}

Text string value. May include only characters which are valid in HTTP paths.

## Default {#section-c5296f4e52394984bf1c0d265ecde940}

None. Each catalog must have a unique `attribute::RootId` value. [!DNL default.ini] typically has an empty `attribute::RootId`.

## See also {#section-5297eaaf736b4db5901e0b37e7cb8bbe}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md) , [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
