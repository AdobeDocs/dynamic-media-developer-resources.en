---
description: For advanced applications it is possible to use the result of a render operation as a material image, just like an image obtained from Image Serving.
solution: Experience Manager
title: Nested Image Rendering requests
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
---
# Nested Image Rendering requests{#nested-image-rendering-requests}

For advanced applications it is possible to use the result of a render operation as a material image, just like an image obtained from Image Serving.

A render request can be used as a material image by specifying it in the `src=` command as follows:

` …&src=ir{ *[!DNL renderRequest]*}&…`

The `ir` token is case-sensitive.

The nested request must not include the Image Rendering root path (typically `http:// *[!DNL server]*/ir/render/'`), but may include pre-processing rule tokens.

The following commands are ignored when specified in nested requests (either in the request url or in `catalog::Modifier` or `catalog::PostModifier`):

* `fmt=` 
* `qlt=` 
* `icc=` 
* `iccEmbed=` 
* `printRes=` 
* `req=` 
* `bgc=`

Also ignored are `attribute::MaxPix` and `attribute::DefaultPix` of the material catalog that applies to the nested render request.

The image result of a nested IR request can be cached optionally by including `cache=on`. By default, caching of intermediate data is disabled. Caching should be enabled only when the intermediate image is expected to be reused in a different request within a reasonable time period. Standard server-side cache management applies. Data is cached in a lossless format.
