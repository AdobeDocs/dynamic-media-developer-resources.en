---
title: op_sharpen
description: Sharpen image. Applies a basic sharpening filter to the layer or to the final view image, after all scaling, if layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
TQID: https://experienceleague.adobe.com/0DZQkJLUEpD1b4kzC07g-9Z44CB-08rc4Q6ljPycFsw
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
# op_sharpen{#op-sharpen}

Sharpen image. Applies a basic sharpening filter to the layer or to the final view image, after all scaling, if layer=comp.

 `op_sharpen=0|1`

The layer mask or composite mask is sharpened as well.

## Properties {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Layer attribute or view attribute. Applies to the current layer or to the final view image if `layer=comp`. Ignored by effect layers.

## Default {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, for no sharpening effect.

## Example {#section-3202122df5db4e14b358ecabfb6d8b85}

Compensate for the slight blurriness caused by image resampling. We also increase the JPEG quality to avoid additional JPEG artifacts along the sharpened edges.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## See also {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
