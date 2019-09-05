---
description: Image (default). Requests standard image data.
seo-description: Image (default). Requests standard image data.
seo-title: img
solution: Experience Manager
title: img
topic: Scene7 Image Serving - Image Rendering API
uuid: 76ba6690-7fd5-4846-a86a-c6fbc1e7f8af
index: y
internal: n
snippet: y
---

# img{#img}

Image (default). Requests standard image data.

 `req=img`

The reply data format and response MIME type are determined by `fmt=`. `req=img` is the default request type and does not need to be specified explicitly. The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

Other request commands are applied as documented. 
