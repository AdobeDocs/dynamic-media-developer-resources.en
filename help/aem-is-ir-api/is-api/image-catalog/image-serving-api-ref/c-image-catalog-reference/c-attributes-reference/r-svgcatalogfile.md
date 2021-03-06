---
description: SVG data file paths. Specifies the files containing the SVG data for this catalog.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
---
# SvgCatalogFile{#svgcatalogfile}

SVG data file paths. Specifies the files containing the SVG data for this catalog.

SVG data files are loaded after all image data files, in the exact order specified. If the same `catalog::Id` value occurs in more than one record (either in the same or different image or SVG catalog files), the last instance prevails.

## Properties {#section-fc2d549f76474792837b2b92ec2087ea}

One or more text string values, separated by commas. Optional. Each value must be an absolute file path or path relative to the catalog folder.

## Default {#section-a4e58951f3c249599665b823566433c9}

Empty, which indicates that this image catalog does not include any SVG data.

## See also {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Catalog Data](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
