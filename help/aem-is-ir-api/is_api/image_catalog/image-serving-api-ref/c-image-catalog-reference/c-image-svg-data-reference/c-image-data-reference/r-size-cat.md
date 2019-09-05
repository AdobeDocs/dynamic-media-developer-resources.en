---
description: Image size. Pixel size of the full-resolution image referenced by catalog Path.
seo-description: Image size. Pixel size of the full-resolution image referenced by catalog Path.
seo-title: Size
solution: Experience Manager
title: Size
topic: Scene7 Image Serving - Image Rendering API
uuid: 36a753fd-9939-4f17-a5d9-7292928907c4
index: y
internal: n
snippet: y
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

[catalog::Path](../../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](r_res.md#reference_3D6FE416801148DEA0F786F2B5169E55) 
