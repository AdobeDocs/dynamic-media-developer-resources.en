---
description: Property data consists of a text string representing one or more properties.
seo-description: Property data consists of a text string representing one or more properties.
seo-title: Property data
solution: Experience Manager
title: Property data
topic: Scene7 Image Serving - Image Rendering API
uuid: 2e51c145-d3d9-4d16-8b25-94fcecb86058
index: y
internal: n
snippet: y
---

# Property data{#property-data}

Property data consists of a text string representing one or more properties.

A property consists of a property name and a property value, separated by =.

Multiple properties are separated by line separators, which may be either `??` or `<CR><LF>`. If the entire property data string is not enclosed in quotation marks, the server replaces each occurrence of `??` with `<CR><LF>` before transmitting the data to the client. Property names may consist of letters, numbers, '.', '-', and '_'. Property names are not case sensitive.

Property values must not include line separators.

See [Text String](../../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) for additional rules applied to Property Data. 
