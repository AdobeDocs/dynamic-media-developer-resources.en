---
description: Four general types of production vignettes are supported.
solution: Experience Manager
title: Vignette scaling
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
TQID: 'https://experienceleague.adobe.com/wyDLZwxCnjFWoMtnYBHVDONCy551mbAruNRRuqrEaGE'
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
# Vignette scaling{#vignette-scaling}

Four general types of production vignettes are supported.

* Single-resolution

  Recommended only when it is certain that only a single render image size is required. 
* Multi-resolution

  Recommended when all desired render image sizes are known. Provides better quality and faster rendering than single-resolution and pyramid vignettes because the image does not need to be scaled after rendering. 
* Pyramid

  Best all purpose, recommended when multiple image sizes are needed and the exact sizes are not pre-determined and when the Dynamic Media Zoom viewer is used. 
* Pyramid with one or more additional resolutions

  Provides high quality for specific sizes while still providing flexibility and zoom viewer support.

Effectively, each resolution is saved to the production vignette as an independent view with its own image width and height.

The view size of a single-resolution vignette is specified with either `-width` or `-height` or both. If both values are specified, the vignette is scaled so that neither dimension is larger than the specified size. If neither value is specified, the output vignette has the same size as the input vignette. No upscaling is applied; if the specified size is larger than the size of the input vignette, the output vignette has the same size as the input vignette.

Effectively the same rules apply to multi-resolution vignettes, with the first resolution level being sized just like a single-resolution vignette. The additional resolutions are specified with additional comma-separated values for either `-width` or `-height`. Values do not need to be sorted. If `-width` specifies multiple values, then `-height` must only provide a single value, and vice versa, otherwise an error is returned.

A pyramid vignette is created by specifying `-pyramid`. The largest resolution level of a such a vignette is determined exactly as for a single-resolution vignette. The additional resolution levels are determined automatically by scaling each level to 0.5x the previous level, with the smallest level not exceeding 128x128 pixels.

Additional resolution levels may be specified for a pyramid vignette, just like for a multi-resolution vignette.

