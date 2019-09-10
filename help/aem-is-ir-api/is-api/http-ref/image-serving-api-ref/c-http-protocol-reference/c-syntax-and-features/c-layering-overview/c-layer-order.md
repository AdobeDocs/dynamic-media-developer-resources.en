---
description: The layer number also determines the z-order.
seo-description: The layer number also determines the z-order.
seo-title: Layer order
solution: Experience Manager
title: Layer order
topic: Scene7 Image Serving - Image Rendering API
uuid: 090f3873-8355-4b11-b05f-f34c74f02a5b
index: y
internal: n
snippet: y
---

# Layer order{#layer-order}

The layer number also determines the z-order.

Layer 0 (the background layer) is required; other layer numbers do not need to be consecutive and will be drawn on top of the background layer, in order of ascending layer number. The layer with the highest layer number is rendered on top and is never occluded by other layers. 
