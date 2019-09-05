---
description: If req=img, the size of the compositing canvas is determined entirely by the size of layer 0.
seo-description: If req=img, the size of the compositing canvas is determined entirely by the size of layer 0.
seo-title: The compositing canvas
solution: Experience Manager
title: The compositing canvas
topic: Scene7 Image Serving - Image Rendering API
uuid: bd750169-4602-4314-9635-3723f3338124
index: y
internal: n
snippet: y
---

# The compositing canvas{#the-compositing-canvas}

If req=img, the size of the compositing canvas is determined entirely by the size of layer 0.

If the `size=` for layer 0 is not specified explicitly, the layer transforms are used to calculate the size of the compositing canvas (see below).

If `req=tmb`, the size of the compositing canvas is determined by the `size=` specified for layer 0, or, if size is not specified, the compositing canvas size is set to the view rect (see below). 
