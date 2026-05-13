---
description: Watermark selector. Specifies the catalog Id of the catalog record to be used as a watermark image or template.
solution: Experience Manager
title: Watermark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
TQID: 'https://experienceleague.adobe.com/zajYc7BBw0BfJ6qvnTFiHY79quRa91-LdY3j1YynxVc'
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
# Watermark{#watermark}

Watermark selector. Specifies the catalog::Id of the catalog record to be used as a watermark image or template.

 If specified, the server applies the watermark to the requested image data for all image requests ( `req=img`).

## Properties {#section-fad6ffff4c5f4b5c8010281bc1377055}

Text string. If specified, must be a valid `Catalog::Id` value in this image catalog (or in the default catalog, if specified in [!DNL default.ini]).

## Default {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Inherited from `default::Watermark` if not defined. If defined but empty, no watermarking is applied for this image catalog, even if `default::Watermark` is defined.

## See also {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
