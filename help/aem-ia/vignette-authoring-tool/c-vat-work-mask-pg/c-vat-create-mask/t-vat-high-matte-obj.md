---
description: A highlight matte object is a special type of overlap object.
seo-description: A highlight matte object is a special type of overlap object.
seo-title: Creating a Mask for a Highlight Matte Object
solution: Experience Manager
title: Creating a Mask for a Highlight Matte Object
topic: Scene7 Image Authoring
uuid: 1b024ca4-f17c-4391-9b45-eb4d6619bc45
index: y
internal: n
snippet: y
---

# Creating a Mask for a Highlight Matte Object{#creating-a-mask-for-a-highlight-matte-object}

A highlight matte object is a special type of overlap object.

It overlays the entire vignette. For most object types, you mask the entire outline of each object. For highlight matte objects, you specify areas of brightness and, within those, specific highlights. You distinguish between these areas by their degree of opacity.

You can use the [ [!DNL Trace] tool](../../c-vat-work-mask-pg/c-vat-mask-pg-tools/c-vat-trace-tool.md#concept-8bcad263ddac45e084f0e22e8adb231c) or the [ [!DNL Mask Brush]](../../c-vat-work-mask-pg/c-vat-mask-pg-tools/c-vat-mask-brush.md#concept-8a63068b04084b57a4f1ed8fd27fcb72) to create the mask for a highlight matte object. Other [!DNL Mask] page tools do not support opacity.

You cannot use the Add or Subtract controls when you define the mask for a highlight mask object. To subtract from a mask area you've defined, set the [!DNL Opacity] slider to zero and brush over that area.

**To Create a Mask for a Highlight Matte Object:** 

1. [Create a highlight matte object](../../c-vat-obj-pg/c-vat-create-grps-obj/t-vat-create-matte-obj.md#task-95a6b27a6c324b81b522bf66a8dc8ed6) on the [!DNL Object] page.
1. On the [!DNL Mask] page, choose the highlight matte object from the [ [!DNL Select Object] box](../../c-vat-gs/c-vat-sel-obj/c-vat-sel-object-box.md#concept-d127c6efaabd436a96c02f36a7bce6ac).
1. Select the **[!UICONTROL Trace]** tool ![](assets/trace.png) or **[!UICONTROL Mask]** Brush ![](assets/mask_brush.png).
1. Set the [!DNL Opacity] slider for the broad areas of brightness. Usually this is a setting of approximately 50%.
1. Define the areas of brightness for the image.

   You can define multiple, separate areas. Don't change the [!DNL Feather] setting to anything but zero, the highlighting feather the edges. 

1. Set the [!DNL Opacity] slider for the highlights within the areas of brightness. Usually this is a setting of approximately 100%.
1. Define the highlights within the areas of brightness.

   Usually these are small areas centered within the broader areas of brightness, indicating the reflection of a point of light.

   Once you've defined the two extremes on the [!DNL Opacity] slider, you can press the plus (+) and minus (-) keys in the numeric keypad on your keyboard to move between them. 

