---
title: Nested Image Rendering requests
description: For advanced applications, it is possible to use the result of a render operation as a material image, just like an image obtained from Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
TQID: 'https://experienceleague.adobe.com/Fqiu-HsaRtrWMjBQudUBzr1iu3WLg7173Kf-71ikejI'
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
# Nested Image Rendering requests{#nested-image-rendering-requests}

For advanced applications, it is possible to use the result of a render operation as a material image, just like an image obtained from Image Serving.

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

The image result of a nested IR request can be cached optionally by including `cache=on`. By default, caching of intermediate data is disabled. Caching should be enabled only when the intermediate image is reused in a different request within a reasonable time period. Standard server-side cache management applies. Data is cached in a lossless format.

