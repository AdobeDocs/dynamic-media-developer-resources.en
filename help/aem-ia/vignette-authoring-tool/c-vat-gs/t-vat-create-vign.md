---
description: Once you have prepared your image, bring it into Image Authoring by creating a vignette and importing the view image.
seo-description: Once you have prepared your image, bring it into Image Authoring by creating a vignette and importing the view image.
seo-title: Creating a Vignette
solution: Experience Manager
title: Creating a Vignette
topic: Scene7 Image Authoring
uuid: c5464b09-d82f-4d14-8392-ca1756761cc8
---

# Creating a Vignette{#creating-a-vignette}

Once you have prepared your image, bring it into Image Authoring by creating a vignette and importing the view image.

 **To Create a Vignette:** 

1. On the [!DNL File] menu, click **[!UICONTROL New]**.
1. In the [!DNL Vignette Properties] dialog box, type a name for the vignette.

   The name of the vignette appears in the title bar when you open this vignette. 

1. To use a [template](../c-vat-gs/t-vat-vign-temp.md#task-0fcd55117eb947808d402cefa8df0c3a) with this vignette, choose it from the list.
1. Choose 2D or 3D for this vignette.

   Choose 2D for vignettes displaying apparel, linens, and so on (without surrounding room scenes). Choose 3D for vignettes with three-dimensional items such as furniture or room scenes.

   A 3D object can reflect light and other objects in the vignette. In order for the 3D mode to have any effect, you must [set up the geometry](../c-vat-3d-mod-pg/c-vat-create-geo/c-vat-abt-geo.md#concept-5d07c29f27834afe8e46852c7c71db9c) for the vignette and associate the 3D objects with geometry. 

1. Specify whether to embed the images for [saved materials](../c-vat-rend-pg/c-vat-rend-tools/t-vat-saved-mat-tool/t-vat-saved-mat-tool.md#task-2f7dd900c44e42f4a8e7f41a3003e2fa) in the vignette file.

   If you check this box, copies of all texture and decal images placed in the [!DNL Saved Materials] list (on the [!DNL Render] page) are saved with the [!DNL .vnt] file in lossless PNG format, for easier transition to the [!DNL Image Renderer]. You can turn off this embedding behavior at any time without loss of information. You cannot embed information for cabinet, door, or window covering materials.

   If [!DNL Image Authoring] needs more information about the [resolution](../c-vat-rend-pg/c-vat-work-text/c-vat-text-mat-prop/c-vat-text-mat-prop.md#concept-56e919cfd48748169dc2f011aa95c5fd) of these material images, it prompts you.

   If you check this box, be careful when adding these materials to the [ [!DNL Favorite Materials]](../c-vat-rend-pg/c-vat-rend-tools/c-vat-fav-mat-tool/c-vat-fav-mat-tool.md#concept-5b0d4a25b5ca49129977e1c8bd266370) list or using materials from the [ [!DNL Material History]](../c-vat-rend-pg/c-vat-rend-tools/t-vat-mat-hist-tool.md#task-95e1391588974719bbf93850448d547b) because [!DNL Image Authoring] may not be able to find them. 

1. Click the **[!UICONTROL Color]** tab in the [!DNL Vignette Properties] dialog box and choose a working color space.

   All ICC RGB color spaces found in your [!DNL system32\spool\drivers\color] directory appear in this list. Changing the color space does not change any color information in your vignette, but it does change the way that colors appear on your monitor. This setting affects the current vignette only and is saved with the vignette. You can also [set a default color space](../c-vat-img-auth-opt/t-vat-color-pref.md#task-b73fd4722e9247e8bce1f5a70518c33d) for all sessions of [!DNL Image Authoring]. If you [export a vignette to an image format](../c-vat-vign-img-rend/t-vat-exp-vign-img-file.md#task-18c83bf6c1ff4c879fc87939835c3e44), you can embed this color space or convert to another one.

   You can [proof the color space](../c-vat-gs/c-vat-abt-color-mgmt/c-vat-abt-color-mgmt.md#concept-2a2d355fd8e841ca95a926397aed4cab) to see what looks best for this image on your monitor. 

1. Click **[!UICONTROL OK]**.

   The [!DNL View Properties] dialog box appears. In the [!DNL View Properties] dialog box, click the **[!UICONTROL General]** tab, then click **[!UICONTROL Action]**. Select [!DNL Load from File] to select your view image. Navigate to the folder that contains the image you want to use, select the image, click **[!UICONTROL Open]**.

   You can [set a preference](../c-vat-img-auth-opt/t-vat-prev-img.md#task-f2c5deb580cb465ebe19f4415bcca037) that displays previews of images in this dialog box. 

1. Name your view image and set any [default resolution and render settings](../c-vat-obj-pg/c-vat-abt-obj-prop/c-vat-view-prop.md#concept-8a396f7b144c46c4806c8ed26619eed1).
1. Click **[!UICONTROL OK]**.

>[!MORE_LIKE_THIS]
>
>* [Changing the Size of a Vignette](../c-vat-gs/t-vat-change-vign-size.md#task-b15e609cb728471da84df99c9878f80b)
>* [Saving Your Work](../c-vat-gs/c-vat-save-work.md#concept-53c6bb778cb949b082477c42839a60f2)
