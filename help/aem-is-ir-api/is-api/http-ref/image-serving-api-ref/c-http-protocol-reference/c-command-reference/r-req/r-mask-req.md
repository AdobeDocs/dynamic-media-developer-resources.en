---
description: Image mask. Requests the mask (alpha channel) data.
seo-description: Image mask. Requests the mask (alpha channel) data.
seo-title: mask
solution: Experience Manager
title: mask
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# mask{#mask}

Image mask. Requests the mask (alpha channel) data.

 `req=mask`

Supports the same commands as `req=img`, and is processed the same way by the server, but instead of returning the RGB or RGBA data, the server discards the color information and returns only the mask (alpha channel) data. The reply data format and response MIME type are determined by `fmt=`.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`. 
