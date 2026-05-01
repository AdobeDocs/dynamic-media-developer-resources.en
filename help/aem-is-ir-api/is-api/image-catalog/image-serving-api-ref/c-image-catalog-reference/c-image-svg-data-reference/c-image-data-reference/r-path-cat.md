---
description: Image file path.
solution: Experience Manager
title: Path
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
TQID: https://experienceleague.adobe.com/AMdTEsCr6sTaAyFYY9c3lEiCUxfZW0ua-KQY5NbtROk
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
# Path{#path}

Image file path.

Relative or absolute path and name of the source image file associated with this catalog record. The server uses the path resolution rules described in Managing Source Data to find the data file.

## Properties {#path-properties}

Text string. Required for image records, may be empty for template records. If specified, it must be a valid relative or absolute Image Server file path. attribute::DefaultExt is appended if no file suffix is present.

## Supported Image File Formats {#path-supported-image-file-formats}

Refer to the description of the Image Converter (IC) utility for a complete list of supported file formats.

Applications that require image ata in multiple different resolutions perform best when using the Dynamic Media pyramid TIFF (PTIFF) multi-resolution format. The IC utility is used to create PTIFF images from any supported image format.

## Default {#path-default}

None.

## See also {#path-seealso}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
