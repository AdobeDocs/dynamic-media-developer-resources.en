---
description: The Highlight tool lets you create areas of brightness for vignettes containing a highlight matte object.
seo-description: The Highlight tool lets you create areas of brightness for vignettes containing a highlight matte object.
seo-title: The Highlight Tool
solution: Experience Manager
title: The Highlight Tool
topic: Scene7 Image Authoring
uuid: 0af5694d-1d0f-4b67-983a-173e90dadba0
---

# The Highlight Tool{#the-highlight-tool}

The Highlight tool lets you create areas of brightness for vignettes containing a highlight matte object.

You begin by creating a normal illumination map for your vignette. You make a copy of this illumination map and adjust it for the highlight matte object.

**To Create Areas of Brightness for Vignettes Containing a Highlight Matte Object:** 

1. [Create a normal illumination map](../../c-vat-work-illum-pg/c-vat-work-illum-maps/t-vat-illum-map-img-auth.md#task-0342a45d98cd456aa4e7cbff6a46ca47) for the entire vignette.
1. With `<none>` selected in the [ [!DNL Select Object] box](../../c-vat-gs/c-vat-sel-obj/c-vat-sel-object-box.md#concept-d127c6efaabd436a96c02f36a7bce6ac), choose **[!UICONTROL Object Properties]** from the [!DNL Edit] menu.
1. Click the **[!UICONTROL Illumination]** tab.
1. Click the **[!UICONTROL Action]** button for Map B or Map C.
1. Choose **[!UICONTROL Copy illum map A]**.
1. Click **[!UICONTROL OK]**.
1. In the side menu, click the **[!UICONTROL Highlight]** tool ![](assets/highlight.png).
1. Select an object or group in the [ [!DNL Select Object] box](../../c-vat-gs/c-vat-sel-obj/c-vat-sel-object-box.md#concept-d127c6efaabd436a96c02f36a7bce6ac).

   Select the object or group that is to be highlighted. You cannot select the highlight matte object itself, because it is not a renderable object. 

1. Click **[!UICONTROL Generate from Matte]**.
1. Use the [!DNL Base Illumination Brightness] and [!DNL Contrast] sliders to adjust the overall illumination for the selected group or object.
1. Use the [!DNL Intensity], [!DNL Radius], and [!DNL Gradient] sliders to adjust the illumination for the selected object.

   To adjust a highlight area that you created when you [masked the highlight matte object](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-high-matte-obj.md#task-a999ee1887384d16ba39dc763ed0c774), hover over that area until you see the grab cursor. Click to select it. Changes to these sliders affect the selected highlight area only. To return to editing the selected object as a whole, click outside the highlight area. 

1. When you are satisfied with the effect, click **[!UICONTROL Apply]**. To adjust the illumination further, after you click **[!UICONTROL Apply]**, click **[!UICONTROL Generate from Matte]** again and repeat the process.
