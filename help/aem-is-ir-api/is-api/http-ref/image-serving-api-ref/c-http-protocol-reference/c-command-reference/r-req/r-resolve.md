---
description: Debug request. This debug command parses and preprocesses the request, execute image catalog lookups, catalog Modifier inclusions, macro and variable substitutions, etc, just like req=img.
seo-description: Debug request. This debug command parses and preprocesses the request, execute image catalog lookups, catalog Modifier inclusions, macro and variable substitutions, etc, just like req=img.
seo-title: resolve
solution: Experience Manager
title: resolve
topic: Scene7 Image Serving - Image Rendering API
uuid: bd1576a7-4802-4a87-b1c0-406f51382561
---

# resolve{#resolve}

Debug request. This debug command parses and preprocesses the request, execute image catalog lookups, catalog::Modifier inclusions, macro and variable substitutions, etc, just like req=img.

 `req=resolve`

The final request string is returned, instead of the result image, with MIME type `text/plain`.

The HTTP response is not cacheable. 
