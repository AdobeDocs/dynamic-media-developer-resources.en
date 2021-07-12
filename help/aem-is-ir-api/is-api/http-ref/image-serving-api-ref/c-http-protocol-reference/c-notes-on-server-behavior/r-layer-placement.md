---
description: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
title: Layer placement
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
---
# Layer placement{#layer-placement}

Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.

 If the layer origin is not specified explicitly for an image layer, it is calculated as follows:

1. Determine the image anchor. Use `anchor=`, or, if not specified, `catalog::Anchor`. 
1. If the image anchor is defined, apply the layer transforms and `extend=` to convert it to an origin= value. 
1. If no image anchor is defined, the layer origin is placed at the center of the layer rectangle (after applying `extend=`).

![](assets/layerplacement.png)
