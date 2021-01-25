---
description: Image data is returned if a request successfully completes, and if the request either does not include a req= command, or if req=img or req=tmb.
seo-description: Image data is returned if a request successfully completes, and if the request either does not include a req= command, or if req=img or req=tmb.
seo-title: Images
solution: Experience Manager
title: Images
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
---

# Images{#images}

Image data is returned if a request successfully completes, and if the request either does not include a req= command, or if req=img or req=tmb.

The HTTP response MIME type is determined by `fmt=`, or, if `fmt=` is not specified, it is `<image/jpeg>`.

The HTTP response status is '200 OK' if the request method was an unconditional `GET` or `HEAD`.

The server may reply with status '304' (not modified) and not return any image data in response to a conditional `GET` request (which includes a valid `If-Modified-Since` or `If-None-Match` header). 
