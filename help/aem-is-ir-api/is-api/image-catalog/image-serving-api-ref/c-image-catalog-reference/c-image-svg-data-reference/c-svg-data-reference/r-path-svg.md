---
description: Path
solution: Experience Manager
title: Path
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Path{#path}

The server uses the path resolution rules described in [Managing Source Data](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) to find the data file.

## Properties {#section-72d9edc532ad43349afcb4df22e1c692}

Text string. Required for image and SVG records, may be empty for template records. If specified, it must be a valid relative or absolute Image Server file path. attribute::DefaultExt is appended if no file suffix is present.

## Supported image file formats {#section-8d6443c883aa48aaa00316fe9661aaa8}

Refer to the description of the Image Converter (IC) utility for a complete list of supported image file formats.

Applications which require image data in multiple different resolutions will perform best when using the Dynamic Media pyramid TIFF (PTIFF) multi-resolution format. The IC utility is used to create PTIFF images from any supported image format.

## Default {#section-82dad83ec3f84ae8bf2f850b4139f63e}

None.

## See also {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[IC Utility](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [attribute::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [attribute::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0), [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) 
