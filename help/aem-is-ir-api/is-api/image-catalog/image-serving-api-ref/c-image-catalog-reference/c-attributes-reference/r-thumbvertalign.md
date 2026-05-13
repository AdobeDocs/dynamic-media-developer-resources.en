---
description: Vertical alignment for thumbnails. Specifies the vertical alignment of the thumbnail image in the reply image rectangle specified by wid= and hei= or by attribute DefaultThumbPix.
solution: Experience Manager
title: ThumbVertAlign
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bb1aa398-5638-4109-bf05-bc51ace4146d
TQID: 'https://experienceleague.adobe.com/nXtO03u9PYt4WcYfV2hYC-Jv5GanZltT37YJlnOF0YU'
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
# ThumbVertAlign{#thumbvertalign}

Vertical alignment for thumbnails. Specifies the vertical alignment of the thumbnail image in the reply image rectangle specified by wid= and hei= or by attribute::DefaultThumbPix.

 Used only for thumbnail requests ( `req=tmb`).

## Properties {#section-f02c23248e87419caf3d95add51aea1e}

Enum. Permitted values are 1, 2, and 3, for top, center, and bottom alignment, respectively.

## Default {#section-30caa4e772254419ad7a3a89d440666c}

Inherited from `default::ThumbHorizAlign` if not defined or if empty.

## See also {#section-c4cd5209d994498eb56a78fcd5bbdfa4}

[catalog::ThumbType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md) , [attribute::DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
