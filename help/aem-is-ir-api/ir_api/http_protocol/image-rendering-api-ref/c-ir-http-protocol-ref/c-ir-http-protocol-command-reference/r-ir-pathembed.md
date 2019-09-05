---
description: Embed paths data. Specifies whether Photoshop paths embedded in the vignette should be included in the response image.
seo-description: Embed paths data. Specifies whether Photoshop paths embedded in the vignette should be included in the response image.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: 6e2cf7b0-7238-40c9-9c35-168cbe771e9f
index: y
internal: n
snippet: y
---

# pathEmbed{#pathembed}

Embed paths data. Specifies whether Photoshop paths embedded in the vignette should be included in the response image.

 `pathEmbed=0|1`

## Properties {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Request attribute. Ignored if the vignette does not contain paths data. The paths data is scaled to `wid=` and/or `hei=` if necessary.

Ignored if the output image format does not support path embedding. Refer to the description of `fmt=` for a list of output image formats that support path embedding.

## Default {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, for no embedding of paths in output images.

## See also {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [wid=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478) 
