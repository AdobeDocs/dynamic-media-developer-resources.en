---
description: Image size. Pixel size of the full-resolution image referenced by catalog Path.
solution: Experience Manager
title: Size
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
TQID: https://experienceleague.adobe.com/-dvyyOil8u3ZmYeehDD-V77JZAmNKKFM25eBCp--IkY
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
# Size{#size}

Image size. Pixel size of the full-resolution image referenced by catalog::Path.

 If this value is provided, Image Serving uses it to avoid having to open the image to obtain the actual image size.

>[!NOTE]
>
>If `catalog::Size`is provided and is not the same as the actual full-resolution image size, undefined behavior may result.

## Properties {#section-5c914ec8b1444a8e99d811b647cd42a3}

Two integer numbers, each greater than 0, separated by a comma. Optional.

## Default {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

If the field is not present, or if the field is empty, the actual size of the image is used.

## See also {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
