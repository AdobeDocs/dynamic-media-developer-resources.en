---
description: The layer number also determines the z-order.
solution: Experience Manager
title: Layer order
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a8fdd55-6ac1-4bc9-935d-188ee60946d9
TQID: 'https://experienceleague.adobe.com/q1ZeufHRmsl9X7FeYaMuGb5N1plRs5SrE9gtv7SYVCg'
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
# Layer order{#layer-order}

The layer number also determines the z-order.

Layer 0 (the background layer) is required; other layer numbers do not need to be consecutive and are drawn on top of the background layer, in order of ascending layer number. The layer with the highest layer number is rendered on top and is never occluded by other layers.
