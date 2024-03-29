---
description: Font metrics file path. Path and name of a font metrics file, including file suffix.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
---
# MetricsPath{#metricspath}

Font metrics file path. Path and name of a font metrics file, including file suffix.

Used for Adobe Type 1 fonts. If not specified, the server attempts to find a font metrics file in the same folder in which the principal font file is located. An error occurs if a required font metrics file cannot be found at render time.

## Properties {#section-955268c581574875b05253d9e14544f3}

Text string. Optional for Adobe Type 1 files. Must be empty or a valid Image Server file path, either absolute or relative to `attribute::RootPath`.

## Default {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

None.

## See also {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
