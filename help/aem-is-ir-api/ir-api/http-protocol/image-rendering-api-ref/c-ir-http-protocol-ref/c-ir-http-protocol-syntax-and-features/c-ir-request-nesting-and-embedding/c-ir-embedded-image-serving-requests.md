---
title: Embedded Image Server requests
description: An Image Server (IS) request can be used as a material image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
TQID: https://experienceleague.adobe.com/oo0cWNcORCi3aZwfzTtK2O7jAH-y520DWUdY7Zne2LI
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
# Embedded Image Server requests{#embedded-image-server-requests}

An Image Server (IS) request can be used as a material image.

Specify the request in the `src=` command as follows:

` …&src=is( *[!DNL imageServingRequest]*)&…`

The `is` token is case-sensitive.

The nested request must not include the Image Serving root path (typically [!DNL http:// *[!DNL server]*/is/image/"]), but may include pre-processing rule tokens.

The following IS commands are ignored when specified in nested requests (either in the request URL or in `catalog::Modifier` or `catalog::PostModifier`):

* `bgc=` 
* `fmt=` 
* `icc=` 
* `iccEmbed=` 
* `printRes=` 
* `qlt=` 
* `quantize=` 
* `req=`

Also ignored are `attribute::MaxPix` and `attribute::DefaultPix` of the image catalog that applies to the embedded IS request.

If the result image of the nested request includes mask (alpha) data, it is always passed to the material. Use a solid color background image layer to avoid unwanted alpha.

The image result of an embedded IS request can be cached optionally by including `cache=on`. By default, caching of intermediate data is disabled. Caching should be enabled only when the intermediate image is reused in a different request within a reasonable time period. Standard server-side cache management applies. Data is cached in a lossless format.
