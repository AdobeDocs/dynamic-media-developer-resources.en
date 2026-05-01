---
title: pathEmbed
description: Embed paths data. Specifies whether Photoshop paths from the layer 0 source image file should be included in the response image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
TQID: https://experienceleague.adobe.com/0MWT9-sknulLzLBGMABj-n8MiotOLd6X5zNGoagxnl8
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
# pathEmbed{#pathembed}

Embed paths data. Specifies whether Photoshop paths from the layer 0 source image file should be included in the response image.

 `pathEmbed=0|1`

## Properties {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Request attribute. Ignored if the source image does not contain paths data. The paths data is scaled and rotated like the image data. Only paths from the source image of `layer=0` are processed; paths from other layer images are ignored.

Ignored if the output image format does not support path embedding. Refer to the description of `fmt=` for a list of output image formats that support path embedding.

## Restrictions {#section-697cddb79a1542bc8457d2f4f59eec69}

Open Photoshop paths (paths which do not form closed loops) are not supported for embedding into the response image at this time.

## Default {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, for no embedding of paths in output images.

## See also {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
