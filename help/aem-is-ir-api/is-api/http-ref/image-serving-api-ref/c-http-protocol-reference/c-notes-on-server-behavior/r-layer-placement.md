---
title: Layer placement
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
TQID: https://experienceleague.adobe.com/SMf4V0AmxYIi0o0FZhMkRx9pprIxjJjEcCWT2agF1Bo
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
# Layer placement{#layer-placement}

Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.

 If the layer origin is not specified explicitly for an image layer, it is calculated as follows:

1. Determine the image anchor. Use `anchor=`, or, if not specified, `catalog::Anchor`. 
1. If the image anchor is defined, apply the layer transforms and `extend=` to convert it to an origin= value. 
1. If no image anchor is defined, the layer origin is placed at the center of the layer rectangle (after applying `extend=`).

![Layer placement image](assets/layerplacement.png)
