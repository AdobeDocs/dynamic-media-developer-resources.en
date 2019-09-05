---
description: Blend Mode. Specifies the type of blending used when the layer is composited. Simulates commonly used blend modes available in Photoshop. Refer to Photoshop documentation for details.
seo-description: Blend Mode. Specifies the type of blending used when the layer is composited. Simulates commonly used blend modes available in Photoshop. Refer to Photoshop documentation for details.
seo-title: blendMode
solution: Experience Manager
title: blendMode
topic: Scene7 Image Serving - Image Rendering API
uuid: ae7ed62c-300a-47ca-9b15-c321b570a23e
index: y
internal: n
snippet: y
---

# blendMode{#blendmode}

Blend Mode. Specifies the type of blending used when the layer is composited. Simulates commonly used blend modes available in Photoshop. Refer to Photoshop documentation for details.

 `blendMode=norm|dissolve|lighten|darken|mult|screen`

## Properties {#section-418aad5a417f49929d1953e226e5c8dd}

Layer Attribute. Ignored by `layer=0` and `layer=comp`.

## Default {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## Example {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## See also {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5) 
