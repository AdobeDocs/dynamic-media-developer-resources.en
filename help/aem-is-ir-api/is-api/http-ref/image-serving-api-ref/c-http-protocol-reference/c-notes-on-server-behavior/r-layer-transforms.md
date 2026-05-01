---
description: Transforms are applied to source images and text layers.
solution: Experience Manager
title: Layer transforms
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
TQID: https://experienceleague.adobe.com/JdUCGqUwuSIDsj6Y2rqfniuNK-poA-ATPyoomSUUZso
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
# Layer transforms{#layer-transforms}

Transforms are applied to source images and text layers.

The following operations are applied to source images, in the given order, to achieve the desired spatial relationship with layer 0:

1. Apply `crop=`, if specified. 
1. Scale based on `size=` or, if `size=` is not specified, based on `scale=`, or, if `scale=` is not specified, based on `res=`, or, if `res=`is not specified, use the full resolution source image. 
1. Apply `flip=`, if specified. 
1. Apply `rotate=`, if specified. 
1. Apply `extend=`, if specified. 
1. Position the layer in the canvas based on `origin=` and `pos=` (see below).

The following transforms are applied to text layers:

1. The text box size is determined by `size=`, or the text width and height, if `size=` is only partially or not at all provided. The text is aligned within the text box using the rtf text alignment attributes. Text may be cropped by the text box. 
1. Scale the text content based on the resolution specified with `textAttr=`. 
1. Apply `rotate=`, if specified. 
1. Apply `extend=`, if specified. 
1. Position the layer in the canvas based on `origin=` and `pos=`(see below).

For both image and text layers, the last step-positioning the layer in the canvas-does not apply to layer 0, since layer 0 effectively constitutes the canvas.
