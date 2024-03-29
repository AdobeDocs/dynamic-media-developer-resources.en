---
description: Catalog record identifier
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
---
# Id {#id}

Index key value by which records in the image data file are looked up by the [!DNL Platform Server].

Typically, a short and unique image identifier, such as a SKU number, possibly with some sort of image suffix, if a SKU has multiple images. May also be a more complex string that looks more like a file path, to support easy retro-fitting of web sites with Image Serving.

## Properties {#id-properties}

Text string. Required. Primary index key for the image data table. Each catalog::Id value must be unique within the table.

## Default {#id-default}

None.

## See also {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
