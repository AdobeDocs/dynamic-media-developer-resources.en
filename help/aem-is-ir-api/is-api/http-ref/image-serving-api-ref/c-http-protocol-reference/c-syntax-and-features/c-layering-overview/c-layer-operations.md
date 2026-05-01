---
description: In addition to sizing (size=) and positioning (pos=) layers relative to layer 0 and specifying the compositing order (the z-order) with the layer= command, layers can be rotated (rotate=) and flipped (flip=).
solution: Experience Manager
title: Layer operations
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
TQID: https://experienceleague.adobe.com/5V4gDi9TiB2Qb6dpfOJlb2vjkOVTPLdNdR0XhumxrdY
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Layer operations{#layer-operations}

In addition to sizing (size=) and positioning (pos=) layers relative to layer 0 and specifying the compositing order (the z-order) with the layer= command, layers can be rotated (rotate=) and flipped (flip=).

The `origin=` and `anchor=` attributes may be used to maintain the desired alignment between layers when images or text are changed dynamically in templates.

The `maskUse=` command is available for image layers to access the background area of images which have separate masks.

`opac=` can be used to vary the layer opacity, and `hide=` to show or hide the layer.
