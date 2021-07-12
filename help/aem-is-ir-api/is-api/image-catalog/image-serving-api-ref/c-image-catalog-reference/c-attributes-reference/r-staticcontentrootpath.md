---
description: Static content data root path. Absolute path or relative path segment for the root folder for the static content data of this image catalog.
solution: Experience Manager
title: StaticContentRootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55ca44cd-4330-47e6-94cc-58c078d34bbd
---
# StaticContentRootPath{#staticcontentrootpath}

Static content data root path. Absolute path or relative path segment for the root folder for the static content data of this image catalog.

See [Managing Source Data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) for additional information about server root paths.

## Properties {#section-f8e3986096294b36948d43aafdc3e795}

Text string. Must be empty, a valid relative file path segment, or an absolute path. Should not include leading and trailing path element delimiters.

## Default {#section-0f741f90fd8d4758a43162c2b5c8a3a3}

Inherited from `default::StaticContentsRootPath` if not defined. If defined but empty, will not contribute to the source file root path.

## See also {#section-9af8846d20d242789df67877f84ed8a7}

[PS::staticContent.rootPaths](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-staticcontentrootpath.md#reference-a2b5368d078349828d282357681bb2a5) ,  [Managing Source Data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)
