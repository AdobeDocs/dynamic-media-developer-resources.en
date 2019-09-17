---
description: Image data file paths. Specifies the files that contain the image data for this catalog.
seo-description: Image data file paths. Specifies the files that contain the image data for this catalog.
seo-title: CatalogFile
solution: Experience Manager
title: CatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 3599c8d3-dc4b-434e-8b11-775ea6f155ee
---

# CatalogFile{#catalogfile}

Image data file paths. Specifies the files that contain the image data for this catalog.

Image data files are loaded in the order specified. If the same `catalog::Id` value occurs in more than one record (either in the same or different catalog files), the last instance prevails.

## Properties {#section-6da55f145ecd4e31a5de52637a436983}

One or more text string values, separated by commas. Optional. Each value must be an absolute file path or path relative to the catalog folder.

## Default {#section-80f91cd7a6b2479ebb310319e9c74da7}

Empty, which indicates that this image catalog does not include any image data.

## See also {#section-910b67c5041d44d99a105ad43ff63a37}

[Catalog Data Fields](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29) 
