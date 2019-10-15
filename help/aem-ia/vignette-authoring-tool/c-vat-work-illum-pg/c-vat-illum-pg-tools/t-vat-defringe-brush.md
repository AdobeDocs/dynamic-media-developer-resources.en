---
description: The Defringe Brush can be used to reduce the contrast of pixels at the edge of light and dark areas (areas where the mask is less than 100%).
seo-description: The Defringe Brush can be used to reduce the contrast of pixels at the edge of light and dark areas (areas where the mask is less than 100%).
seo-title: The Defringe Brush
solution: Experience Manager
title: The Defringe Brush
topic: Scene7 Image Authoring
uuid: 8b6a92d0-4709-4643-b50b-2e0fdbfd28d1
---

# The Defringe Brush{#the-defringe-brush}

The Defringe Brush can be used to reduce the contrast of pixels at the edge of light and dark areas (areas where the mask is less than 100%).

Such objects display a halo when they are rendered, because the mask edges don't quite align with the illumination effect. This can happen when you import an illumination map from another source. The [!DNL Defringe Brush] makes the illumination map align more closely to the mask.

You can apply the [!DNL Defringe Brush] to an entire group or to a single object. If you apply it to a group, it affects only the edges of the entire group, and does not affect edges inside the group. You cannot apply the [!DNL Defringe Brush] to non-renderable objects.

The [!DNL Defringe Brush] is most effective for separating objects to which you plan to apply different materials.

If a particular object's illumination map should have more contrast at its edges, you can specify a threshold contrast below which the [!DNL Defringe Brush] does not apply.

**To Apply the Defringe Brush:** 

1. Select an object or group in the [ [!DNL Select Object] box](../../c-vat-gs/c-vat-sel-obj/c-vat-sel-object-box.md#concept-d127c6efaabd436a96c02f36a7bce6ac).
1. In the side menu, click the **[!UICONTROL Defringe Brush]** ![](assets/defringe.png).
1. In the image, drag the brush over the edge you want to clean up.
You can set the following options for the [!DNL Defringe Brush]:

* **Contrast Threshold:** Limits the effect to the edge pixels that have more than the specified contrast level and preserves the edges with less than this level of contrast. The default contrast value of zero reduces the contrast of all edge pixels to zero. 
* **Edge Width:** Limits the effect to the pixels that are within this number of pixels of the edge. 
* **Apply to Whole Object:** Applies your changes to the entire object or group that is currently selected.

