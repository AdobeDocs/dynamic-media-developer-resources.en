---
description: If Photoshop is installed on the same computer as Image Authoring, you can open the current image in Photoshop with a single click, even if Photoshop is not open at the time.
seo-description: If Photoshop is installed on the same computer as Image Authoring, you can open the current image in Photoshop with a single click, even if Photoshop is not open at the time.
seo-title: Editing a Vignette in Photoshop
solution: Experience Manager
title: Editing a Vignette in Photoshop
topic: Scene7 Image Authoring
uuid: f3b059a2-21e3-445a-842a-fc4251fea20f
---

# Editing a Vignette in Photoshop{#editing-a-vignette-in-photoshop}

If Photoshop is installed on the same computer as Image Authoring, you can open the current image in Photoshop with a single click, even if Photoshop is not open at the time.

|  Object Page  | Mask Page  | Illumination Page  |
|---|---|---|
|  View image only  | Current mask object only  | Grayscale image representing the current illumination map.  |
|  | | Any defined masks for the currently selected objects are displayed as separate channels.  |

** **To Edit the Current Image in Photoshop:** ** 

1. Go to the desired location in [!DNL Image Authoring].

   The **[!UICONTROL Edit Image in Photoshop]** button is available on the [!DNL Object], [!DNL Mask], and [!DNL Illumination] pages only. 

1. Select the item to edit.

   On the [!DNL Object] page, the main view is always the item that opens in [!DNL Photoshop], regardless of what is selected.

   On the [!DNL Illumination] page, select the illumination map to edit (if you use multiple illumination maps). The mask for the currently selected object also opens in [!DNL Photoshop]. Only that portion of the image is updated in [!DNL Image Authoring] when you close the image in [!DNL Photoshop]. If you want to edit a larger area, select the entire view.

   On the [!DNL Mask] page, select the masked object to edit.

[!DNL Protect Other Masks] is ignored by [!DNL Photoshop], even if it is checked in [!DNL Image Authoring]. 

1. Click the **[!UICONTROL Edit Image in Photoshop]** button ![](assets/edit.png).
1. Make any changes. You can undo individual changes in [!DNL Photoshop], as you would normally. When you return to [!DNL Image Authoring], you can reverse all your [!DNL Photoshop] edits at once by choosing **[!UICONTROL Undo]**, but you cannot reverse individual changes.
1. In [!DNL Photoshop], from the [!DNL File] menu, close the image in [!DNL Photoshop] and return to [!DNL Image Authoring].
