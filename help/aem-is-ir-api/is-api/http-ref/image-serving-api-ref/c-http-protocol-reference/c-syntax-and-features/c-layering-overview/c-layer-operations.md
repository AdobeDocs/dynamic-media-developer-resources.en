---
description: In addition to sizing (size=) and positioning (pos=) layers relative to layer 0 and specifying the compositing order (the z-order) with the layer= command, layers can be rotated (rotate=) and flipped (flip=).
solution: Experience Manager
title: Layer operations
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
---
# Layer operations{#layer-operations}

In addition to sizing (size=) and positioning (pos=) layers relative to layer 0 and specifying the compositing order (the z-order) with the layer= command, layers can be rotated (rotate=) and flipped (flip=).

The `origin=` and `anchor=` attributes may be used to maintain the desired alignment between layers when images or text are changed dynamically in templates.

The `maskUse=` command is available for image layers to access the background area of images which have separate masks.

`opac=` can be used to vary the layer opacity, and `hide=` to show or hide the layer.
