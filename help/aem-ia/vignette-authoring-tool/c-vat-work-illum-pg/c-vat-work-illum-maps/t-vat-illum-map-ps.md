---
description: An Illumination Map is created automatically by Image Authoring when you create your vignette.
seo-description: An Illumination Map is created automatically by Image Authoring when you create your vignette.
seo-title: Editing an Illumination Map in Photoshop
solution: Experience Manager
title: Editing an Illumination Map in Photoshop
topic: Scene7 Image Authoring
uuid: bb2059cb-7e6f-40e3-be14-a2afb56dde03
index: y
internal: n
snippet: y
---

# Editing an Illumination Map in Photoshop{#editing-an-illumination-map-in-photoshop}

An Illumination Map is created automatically by Image Authoring when you create your vignette.

 [!DNL Image Authoring] includes a number of tools to manipulate the illumination. You may want to fine-tune the [!DNL Illumination Map] using [!DNL Photoshop], or a similar image editing application, if the image contains textures that need to be removed from renderable surfaces.

**To Edit an Illumination Map in Photoshop:** 

1. Open the original image in [!DNL Photoshop] or [export the [!DNL Illumination Map] and any needed masks.](../../c-vat-obj-pg/c-vat-img-maps/t-vat-exp-img-map.md#task-15fc6689062e49b098a698d6621a793b)

   Include any masks you need when editing the [!DNL Illumination Map] in [!DNL Photoshop]. 

1. Adjust the [!DNL Illumination Map] in [!DNL Photoshop], using the imported masks as needed. For example, unless you have a grayscale image, you may want to do the following:

    * Choose **[!UICONTROL Image]** > **[!UICONTROL Adjust]** > **[!UICONTROL Desaturate]**. 
    
    * Choose **[!UICONTROL Image]**> **[!UICONTROL Adjust]**> **[!UICONTROL Levels]** and change the [!DNL Input Levels] and [!DNL Output Levels] as shown in the following table:

       |  Image Type  | Input Levels  | Output Levels  |
       |---|---|---|
       |  Patterned and mid-tone solids  | 30, .6, and 255  | 0 and 200  |
       |  Light-tone solids  | 20, 1, 255  | 0 and 230  |
       |  Dark-tone solids  | 60, .4, 255  | 0 and 200  |

1. Save the resulting 8-bit grayscale image as a [!DNL .PNG] or [!DNL .TIF] file.
1. In [!DNL Image Authoring], Ctrl-click ![](assets/finger.png) in the toolbar to see the [!DNL View Properties] dialog box.
1. Click the **[!UICONTROL Illumination]** tab, click the **[!UICONTROL Action]** button for the [!DNL Illumination Map] you are editing (usually Map A), then select **[!UICONTROL Load From File]**.
1. Choose the illumination file you saved in [!DNL Photoshop], then click **[!UICONTROL OK]**.
You can also try using the [ [!DNL Edit Image in Photoshop]](../../c-vat-gs/c-vat-work-ps/t-vat-edit-vign-ps.md#task-cce73c014f5c4e81bdb5878d3067c809) button on the toolbar. 

>[!MORE_LIKE_THIS]
>
>* [About Illumination Maps](../../c-vat-work-illum-pg/c-vat-abt-illum-pg/c-vat-illum-maps.md#concept-3243a49c92dd4491947481d339d12f3f)
>* [Editing a Vignette in Photoshop](../../c-vat-gs/c-vat-work-ps/t-vat-edit-vign-ps.md#task-cce73c014f5c4e81bdb5878d3067c809)
>* [Importing an Illumination Map](../../c-vat-work-illum-pg/c-vat-work-illum-maps/t-vat-imp-illum-map.md#task-2171a079ad2b45ada70487cbbcff5d89)
