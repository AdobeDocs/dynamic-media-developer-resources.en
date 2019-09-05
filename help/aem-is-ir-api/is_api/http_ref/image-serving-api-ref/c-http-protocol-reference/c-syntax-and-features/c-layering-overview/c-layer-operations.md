---
description: In addition to sizing (size=) and positioning (pos=) layers relative to layer 0 and specifying the compositing order (the z-order) with the layer= command, layers can be rotated (rotate=) and flipped (flip=).
seo-description: In addition to sizing (size=) and positioning (pos=) layers relative to layer 0 and specifying the compositing order (the z-order) with the layer= command, layers can be rotated (rotate=) and flipped (flip=).
seo-title: Layer operations
solution: Experience Manager
title: Layer operations
topic: Scene7 Image Serving - Image Rendering API
uuid: 38786356-29da-49d6-8f5f-234bbf90fa0b
index: y
internal: n
snippet: y
---

# Layer operations{#layer-operations}

In addition to sizing (size=) and positioning (pos=) layers relative to layer 0 and specifying the compositing order (the z-order) with the layer= command, layers can be rotated (rotate=) and flipped (flip=).

The `origin=` and `anchor=` attributes may be used to maintain the desired alignment between layers when images or text are changed dynamically in templates.

The `maskUse=` command is available for image layers to access the background area of images which have separate masks.

`opac=` can be used to vary the layer opacity, and `hide=` to show or hide the layer. 
