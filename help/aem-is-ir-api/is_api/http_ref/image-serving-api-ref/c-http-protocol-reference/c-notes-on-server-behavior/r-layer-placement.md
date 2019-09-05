---
description: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
seo-description: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
seo-title: Layer placement
solution: Experience Manager
title: Layer placement
topic: Scene7 Image Serving - Image Rendering API
uuid: f147d021-3a7b-4b95-9498-0cd2c78ac7c0
index: y
internal: n
snippet: y
---

# Layer placement{#layer-placement}

Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.

 If the layer origin is not specified explicitly for an image layer, it is calculated as follows:

1. Determine the image anchor. Use `anchor=`, or, if not specified, `catalog::Anchor`. 
1. If the image anchor is defined, apply the layer transforms and `extend=` to convert it to an origin= value. 
1. If no image anchor is defined, the layer origin is placed at the center of the layer rectangle (after applying `extend=`).

![](assets/layerplacement.png)

