---
description: Image size. Pixel size of the full-resolution image referenced by catalog Path.
seo-description: Image size. Pixel size of the full-resolution image referenced by catalog Path.
seo-title: Size
solution: Experience Manager
title: Size
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
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
