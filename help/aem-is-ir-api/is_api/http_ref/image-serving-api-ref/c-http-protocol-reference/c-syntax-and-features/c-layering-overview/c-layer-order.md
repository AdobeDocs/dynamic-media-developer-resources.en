---
description: The layer number also determines the z-order.
seo-description: The layer number also determines the z-order.
seo-title: Layer order
solution: Experience Manager
title: Layer order
topic: Scene7 Image Serving - Image Rendering API
uuid: bd410787-5444-4b33-862d-0b2a2c5e6f6a
index: y
internal: n
snippet: y
---

# Layer order{#layer-order}

The layer number also determines the z-order.

Layer 0 (the background layer) is required; other layer numbers do not need to be consecutive and will be drawn on top of the background layer, in order of ascending layer number. The layer with the highest layer number is rendered on top and is never occluded by other layers. 
