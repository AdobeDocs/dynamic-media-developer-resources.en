---
title: RootPath
description: Source data root path. Text string value. Absolute path or relative path segment for the root folder for all vignette, texture, image, and ICC data files referenced by this image catalog.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
TQID: 'https://experienceleague.adobe.com/yCtXjcZDG0HCqydirr7TDe5-e0oWtHmlvAxHDl-gfac'
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
# RootPath{#rootpath}

Source data root path. Text string value. Absolute path or relative path segment for the root folder for all vignette, texture, image, and ICC data files referenced by this image catalog.

## Properties {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Text string. Must be empty, a valid path segment relative to the Image Rendering server configuration setting `ir.resourceRootPaths`, or a valid absolute file path. Should not include leading and trailing path element delimiters.

## Default {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Inherited from `default::RootPath` if not defined. If defined but empty, it does not contribute to the source file root path.

## See also {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`
