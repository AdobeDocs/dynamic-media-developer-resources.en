---
description: Layers are composited in the order specified by the layer= command, where higher-numbered layers hide lower-numbered ones.
solution: Experience Manager
title: The compositing canvas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
TQID: https://experienceleague.adobe.com/SaG-pD7T3xSmLeIESnL0UzODS-2kJb-0jx-A5BxMgOg
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
# The compositing canvas{#the-compositing-canvas}

Layers are composited in the order specified by the layer= command, where higher-numbered layers hide lower-numbered ones.

Layer 0 constitutes the background layer, which is always required and which defines the size of the composite image. Any of the layer types is permitted for layer 0. The size of layer 0 must be defined, either explicitly using `size=` or implicitly, based on the content image or text. Any areas of other layers which fall outside the area of layer 0 are not included in the output image.

>[!NOTE]
>
>After all layers are flattened, the composite image is converted to the final response image, as specified with the [view commands and attributes](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
