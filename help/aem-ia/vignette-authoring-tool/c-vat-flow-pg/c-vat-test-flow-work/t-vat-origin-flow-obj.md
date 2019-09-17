---
description: When you apply a texture to an object, the texture anchor point matches up with the origin to position the texture on the object's surface.
seo-description: When you apply a texture to an object, the texture anchor point matches up with the origin to position the texture on the object's surface.
seo-title: Changing the Origin for Flowline Objects
solution: Experience Manager
title: Changing the Origin for Flowline Objects
topic: Scene7 Image Authoring
uuid: 3e5b537e-60ef-40ac-9155-bbee353cf708
---

# Changing the Origin for Flowline Objects{#changing-the-origin-for-flowline-objects}

When you apply a texture to an object, the texture anchor point matches up with the origin to position the texture on the object's surface.

Each object in a vignette has at least one origin but may have up to six different origins.

Most objects use the standard or center-match origin. Flowline objects may also have [other origins](../../c-vat-flow-pg/c-vat-abt-flow/c-vat-flow-pg-opt.md#concept-ab8e010be60d46c8841f1b00c3501d16).

For apparel objects, you generally use a center-match origin. The position of the origin depends on the type of apparel item you are rendering. Often apparel parts are grouped together. Each group has an explicit origin (for example, the origin for the front of the shirt might be above the solar plexus, while the origin for a sleeve might be outside the biceps). The origin might flow across to other parts (such as cuffs or breast pockets).

For upholstery with a strong pattern, you can use the continuous origin or other origins. Position the origin on the middle of a prominent part, such as the center seat cushion of a sofa, then [connect the other parts](../../c-vat-flow-pg/c-vat-test-flow-work/t-vat-match-text.md#task-568d59da3f7e48838669b17fe96fbed0).

**To Change the Texture Origin for a Flowline Object:** 

1. Select the **[!UICONTROL Texture]** tool ![](assets/texture.png).
1. Check the [!DNL Show Origin] check box to see the intersection point of the green and purple dashed lines that indicate the origin.
1. Drag the intersection of the purple and green dashed lines to move the origin.

   You can also set any of the origins by typing values into the [!DNL Origin] boxes in the side menu. The location of the origin changes when you [match textures on adjacent objects](../../c-vat-flow-pg/c-vat-test-flow-work/t-vat-match-text.md#task-568d59da3f7e48838669b17fe96fbed0).

>[!MORE_LIKE_THIS]
>
>* [About the Origin](../../c-vat-rend-pg/c-vat-work-text/c-vat-abt-origin.md#concept-643d030b62fd42a5bf3ce4e4ab9a3a47)
>* [Matching Up Textures on Adjacent Flowline Objects](../../c-vat-flow-pg/c-vat-test-flow-work/t-vat-match-text.md#task-568d59da3f7e48838669b17fe96fbed0)
