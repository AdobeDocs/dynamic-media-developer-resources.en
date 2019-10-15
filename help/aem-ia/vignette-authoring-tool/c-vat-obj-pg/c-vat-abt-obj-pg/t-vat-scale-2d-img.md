---
description: For 2D vignettes, you can define the scale of objects relative to their size in the real world.
seo-description: For 2D vignettes, you can define the scale of objects relative to their size in the real world.
seo-title: Defining Scale for 2D Images
solution: Experience Manager
title: Defining Scale for 2D Images
topic: Scene7 Image Authoring
uuid: c6599b12-84bf-445a-a8ef-f1e0d7dc3f5b
---

# Defining Scale for 2D Images{#defining-scale-for-d-images}

For 2D vignettes, you can define the scale of objects relative to their size in the real world.

For 3D vignettes, you do this by [defining the size of a single object](../../c-vat-3d-mod-pg/c-vat-create-geo/t-vat-def-3d-scale.md#task-7938e8b9590543a78d48b678d2d26ba9) on the [!DNL 3D Modeling] page.

You can set the view resolution to show the number of pixels in one inch of the real world that the image represents. In order to set this properly, you must know the actual dimensions of an object in the image. Once you set the view resolution, new objects scale properly.

For example, if the image is 800 pixels wide, and a 80"x80" tablecloth takes up half the image, then half the pixel width of the image (400 pixels) is equal to 80 inches in real life. Therefore, you set [!DNL Default Object Resolution] to 5, because 5 pixels represent each inch of the tablecloth width. By default, this option is set to 10.

If you want to set the default view resolution for all vignettes, change the [!DNL Default Object Resolution] value on the [!DNL General] tab of the [!DNL Preferences] dialog box. If you want to set the view resolution for the current vignette only, change the default resolution values on the [!DNL General] tab of the [ [!DNL View Properties] dialog box](../../c-vat-obj-pg/c-vat-abt-obj-prop/c-vat-view-prop.md#concept-8a396f7b144c46c4806c8ed26619eed1).

Once you set this value for the vignette, [!DNL Image Authoring] can set a reasonable size for new objects you create. If you apply only [simple, smooth textures, such as heather fabrics](../../c-vat-rend-pg/c-vat-rend-obj/t-vat-heather-text-eff.md#task-00de2da0ac644349868db8249dd2ab2c), the resolution setting may eliminate the need to create flowlines for the vignette. It does not work for heavy patterns or textures.

**To Set the View Resolution Relative to the Physical Size of Objects:** 

1. From the [!DNL Edit] menu, choose [!DNL Preferences], then click the **[!UICONTROL General]** tab.
1. Change the [!DNL Default Object Resolution] setting to the number of pixels in one inch of a real object in the image.
1. Click **[!UICONTROL OK]**.
