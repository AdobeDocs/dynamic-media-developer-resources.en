---
description: Each sketch line you add to your image is called a feature.
seo-description: Each sketch line you add to your image is called a feature.
seo-title: Creating Sketch Features
solution: Experience Manager
title: Creating Sketch Features
topic: Scene7 Image Authoring
uuid: c8e6b129-3192-4296-a1c8-c90a24368b1b
---

# Creating Sketch Features{#creating-sketch-features}

Each sketch line you add to your image is called a feature.

 Each feature type uses a different color. Try to make sure that features do not overlap. 

|  Feature Style  | Feature Color  | Feature Purpose  | Tips  |
|---|---|---|---|
|  **Warp** | Green solid line  | Defines the vertical direction of the texture.  |Define the [!DNL Warp] and [!DNL Weft] before you define other features. Follow the outside contours of the object. You don't need to draw the full length of the [!DNL Warp] or [!DNL Weft].  |
|  **Weft** | Blue solid line  | Defines the horizontal direction of the texture.  | |
|  **Horizon Edge** | Black and yellow dashed line  | Defines the visible edges of the surface, where the texture disappears behind the object.  |Draw [!DNL Horizon Edges] after you define the [!DNL Warp] and [!DNL Weft]. Draw edges at the edge of the masked area of the object. Draw the entire length of the edges.  |
|  **Cut/Seam** | Black and white dashed line  | Clothing seams, darts, vents, and so on, where the fabric may not line up on either side of the feature line.  |Add [!DNL Cut/Seams] after you add edges. Draw the entire length of the cut, seam, dart, or vent.  |
|  **Fold** | Yellow solid line  |Defines places where the texture folds under itself, and the visible texture may not line up on either side of the feature line. If the texture is obscured by another object, use [!DNL Hidden Area] instead of [!DNL Fold].  |Add [!DNL Folds] and [!DNL Ridges] last. Use either a [!DNL Fold] or a [!DNL Ridge] for peaked areas. Use a [!DNL Fold] if the fabric doesn't line up on either side. You don't need to draw the full length of [!DNL Ridges] or [!DNL Folds].  |
|  **Ridge** | Violet solid line  | Defines places where the texture peaks along the center of the feature line and levels off around its edges.  |Use a [!DNL Ridge] if the fabric lines up on either side.  |
|  **Hidden Area** | Black and white dashed loop  |Defines the perimeter of areas that are hidden by other objects. This prevents the object from being treated as two separate objects and influences the texture distribution on the visible parts of the object. If the fabric is hidden because the object folds over itself, use [!DNL Fold] instead of [!DNL Hidden Area].  | Use this feature to connect parts of a single object that disappear behind another object. For example, if a blouse is partially obscured by a scarf, define the scarf areas as hidden parts of the blouse.  |
|  ** [Object Connector](../../c-vat-work-sketch-pg/r-vat-create-sketch-feat/c-vat-ex-obj-conn-feat.md#concept-e8efd73a0ac34a339be51ba9c377bea3) ** | | Continues a texture seamlessly across adjacent objects.  |You can add one [!DNL Object Connector] feature per object. Solve the underlying object before you solve any connected parts.  |

`<unknown> When you draw a feature other than  <span class="wintitle"> Warp</span> and  <span class="wintitle"> Weft</span>, you draw the feature's centerline.  <span class="keyword"> Image Authoring</span> adjusts the area surrounding the centerline in accordance with the type of feature and the current settings.</unknown>` 