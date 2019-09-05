---
description: Image mask. Requests the mask (alpha channel) data.
seo-description: Image mask. Requests the mask (alpha channel) data.
seo-title: mask
solution: Experience Manager
title: mask
topic: Scene7 Image Serving - Image Rendering API
uuid: ce44f61f-a482-44d6-b58a-3a9a391f4999
index: y
internal: n
snippet: y
---

# mask{#mask}

Image mask. Requests the mask (alpha channel) data.

 `req=mask`

Supports the same commands as `req=img`, and is processed the same way by the server, but instead of returning the RGB or RGBA data, the server discards the color information and returns only the mask (alpha channel) data. The reply data format and response MIME type are determined by `fmt=`.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`. 
