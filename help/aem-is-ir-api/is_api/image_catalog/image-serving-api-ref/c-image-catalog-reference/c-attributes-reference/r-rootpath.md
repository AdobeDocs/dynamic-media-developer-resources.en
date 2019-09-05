---
description: Source data root path. Absolute or relative path for the root folder for the source data of this image catalog.
seo-description: Source data root path. Absolute or relative path for the root folder for the source data of this image catalog.
seo-title: RootPath
solution: Experience Manager
title: RootPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a7a69668-3129-4294-a3b0-029211e35548
index: y
internal: n
snippet: y
---

# RootPath{#rootpath}

Source data root path. Absolute or relative path for the root folder for the source data of this image catalog.

The `RootPath` is a text string value. See [Managing Source Data](../../../../../is_api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) for additional information about server root paths.

## Properties {#section-b41d7e0ea63143eb8034569706cad0c0}

Text string. Must be empty, a valid relative folder path, or a valid absolute path accessible by the Image Server.

## Default {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Inherited from `default::RootPath` if not defined. If defined but empty, will not contribute to the source file root path.

## See also {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](r_path_cat.md#reference_306AFCAFF172440CA81B85DA8D78213C) , [catalog::MaskPath](r_maskpath_cat.md#reference_F82B42535FFF42959E74A7C1E605C931),  [ruleset::PathRule](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Managing Source Data](../../../../../is_api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) 
