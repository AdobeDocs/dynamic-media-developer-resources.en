---
description: The layer number also determines the z-order.
solution: Experience Manager
title: Layer order
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a8fdd55-6ac1-4bc9-935d-188ee60946d9
---
# Layer order{#layer-order}

The layer number also determines the z-order.

Layer 0 (the background layer) is required; other layer numbers do not need to be consecutive and will be drawn on top of the background layer, in order of ascending layer number. The layer with the highest layer number is rendered on top and is never occluded by other layers.
