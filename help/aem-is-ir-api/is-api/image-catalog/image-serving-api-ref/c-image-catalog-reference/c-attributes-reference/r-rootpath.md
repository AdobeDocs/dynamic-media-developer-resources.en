---
description: Source data root path. Absolute or relative path for the root folder for the source data of this image catalog.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# RootPath{#rootpath}

Source data root path. Absolute or relative path for the root folder for the source data of this image catalog.

The `RootPath` is a text string value. See [Managing Source Data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) for additional information about server root paths.

## Properties {#section-b41d7e0ea63143eb8034569706cad0c0}

Text string. Must be empty, a valid relative folder path, or a valid absolute path accessible by the Image Server.

## Default {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Inherited from `default::RootPath` if not defined. If defined but empty, will not contribute to the source file root path.

## See also {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Managing Source Data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) 
