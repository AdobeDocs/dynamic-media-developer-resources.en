---
description: Image file path.
solution: Experience Manager
title: Path
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
---
# Path{#path}

Image file path.

Relative or absolute path and name of the source image file associated with this catalog record. The server uses the path resolution rules described in Managing Source Data to find the data file.

## Properties {#path-properties}

Text string. Required for image records, may be empty for template records. If specified, it must be a valid relative or absolute Image Server file path. attribute::DefaultExt is appended if no file suffix is present.

## Supported Image File Formats {#path-supported-image-file-formats}

Refer to the description of the Image Converter (IC) utility for a complete list of supported file formats.

Applications that require image ata in multiple different resolutions will perform best when using the Dynamic Media pyramid TIFF (PTIFF) multi-resolution format. The IC utility is used to create PTIFF images from any supported image format.

## Default {#path-default}

None.

## See also {#path-seealso}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
