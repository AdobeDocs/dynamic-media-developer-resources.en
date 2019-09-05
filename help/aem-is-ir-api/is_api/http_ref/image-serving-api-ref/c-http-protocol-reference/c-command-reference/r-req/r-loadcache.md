---
description: Preload server cache. Executes the request just like req=img, but instead of returning the image, the server returns the length of the reply image (image.length), formatted as text data with MIME type text/plain.
seo-description: Preload server cache. Executes the request just like req=img, but instead of returning the image, the server returns the length of the reply image (image.length), formatted as text data with MIME type text/plain.
seo-title: loadcache
solution: Experience Manager
title: loadcache
topic: Scene7 Image Serving - Image Rendering API
uuid: eba47bcb-cae6-462f-98f7-4d1f25ea5d69
index: y
internal: n
snippet: y
---

# loadcache{#loadcache}

Preload server cache. Executes the request just like req=img, but instead of returning the image, the server returns the length of the reply image (image.length), formatted as text data with MIME type text/plain.

 `req=loadcache`

The HTTP response is not cacheable.

Other commands in the request apply as documented. 
