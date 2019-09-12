---
description: Use Image Authoring to prepare your window covering.
seo-description: Use Image Authoring to prepare your window covering.
seo-title: Preparing Images for Window Covering Files
solution: Experience Manager
title: Preparing Images for Window Covering Files
topic: Scene7 Image Authoring
uuid: 43eb0a69-41e7-4fea-82cc-b701ec6de152
index: y
internal: n
snippet: y
---

# Preparing Images for Window Covering Files{#preparing-images-for-window-covering-files}

Use Image Authoring to prepare your window covering.

Create, mask, and generate an illumination map for the window-covering image, and draw its flowlines. Then, export the group representing the window-covering image in a special file format that includes all the information you've specified.

If the window covering you are creating comes in pairs (for example, left-hand and right-hand drapes or curtains), you must prepare and export two separate items: the left-hand side and the right-hand side. When you import these into the [!DNL Content Authoring] tool, you merge them to create a single object.

If the window covering you are creating comes in different widths, you can create both a narrow and a wide version. This is optional, and may entail opening and editing two different images. When you import these into the [!DNL Content Authoring] tool, the resulting file contains information about the widths of the two items. When you apply the resulting object in [!DNL Image Authoring], the renderer can judge which one to use, based on the size of the window to which you are applying it.

**To Prepare the Window Covering Files:** 

1. In [!DNL Image Authoring], create a 2D vignette using an image that shows the window covering.

   If the window covering comes in a narrow and wide version, create and export each one separately. This requires two separate groups, one for each version.
1. Create a group that represents the window covering.

   For example, this might be a valance, a set of blinds, and so on.

   If you are creating a window covering that comes in pairs, prepare two groups, one for each half of the pair. 

1. Create flowline objects that represent the components of the window covering.

   For example, you might need separate objects for different layers of a curtain, or different sections of blinds.
1. Adjust the illumination map for the window covering.

   The window covering inherits its illumination and [gloss](../../../r-vat-glossary/c-vat-gloss.md#concept-c935eeb0b63442368231fb26b5a58f50) settings from Map A, so make your adjustments to that map. 

1. On the [!DNL Object] page, right-click the window-covering group in the [!DNL Object Hierarchy] and choose **[!UICONTROL Export VNW File]**. Choose a name and location for the [!DNL .vnw] file.

   The VNW file contains illumination, mask, and flowline information for all the objects in the window-covering group.

   If you created a pair of groups-left-hand and right-hand-export them to separate files.

   If you want to set opacity for this window covering (for example, so that the window covering can display transparency that varies with different layers of fabric), you must create a separate image in [!DNL Photoshop], or some other photo-editing software. This image must specify the opacity areas as the alpha channel. It must be exactly the same size as the image you authored in [!DNL Image Authoring]. 

1. Use the [!DNL Content Authoring] tool to create the window-covering image file.
