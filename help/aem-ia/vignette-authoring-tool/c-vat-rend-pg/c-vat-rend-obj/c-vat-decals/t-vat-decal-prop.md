---
description: You can change information about the decal.
seo-description: You can change information about the decal.
seo-title: Changing a Decal's Properties
solution: Experience Manager
title: Changing a Decal's Properties
topic: Scene7 Image Authoring
uuid: 832d13cf-e8b9-465b-833f-6cd83c76e349
---

# Changing a Decal's Properties{#changing-a-decal-s-properties}

You can change information about the decal.

If you have created a gloss map file, you can apply gloss to the alpha channel specified in that map file, independent of the rest of the decal image. You can also apply a gloss to the entire decal.

** To Change the Properties for a Decal:** 

1. Right-click the object to which you applied the decal and choose **[!UICONTROL Decal]** > **[!UICONTROL Properties]**.
1. In the [!DNL Decal Material Properties] dialog box, click the **[!UICONTROL General]** tab to change information about the fabric.

   **Name/ID:** This is the filename for the decal image without the file extension.

   **Colorize:** Check this box to add a color to the alpha channel of the image. Click the color box to [choose a color](../../../c-vat-rend-pg/c-vat-rend-obj/t-vat-rend-solid-color.md#task-e051bda9851e4c6fb7e33a38b6e47f0d).

   **Preferred Illum Map:** Specify the [ [!DNL Illumination Map]](../../../c-vat-obj-pg/c-vat-abt-obj-prop/c-vat-view-prop.md#concept-8a396f7b144c46c4806c8ed26619eed1) to use for determining the gloss of this image.

   ** [Gloss](../../../r-vat-glossary/c-vat-gloss.md#concept-c935eeb0b63442368231fb26b5a58f50):** Specify the percentage of shininess for this image. This setting, combined with the [ [!DNL Illumination Map]](../../../c-vat-obj-pg/c-vat-abt-obj-prop/c-vat-view-prop.md#concept-8a396f7b144c46c4806c8ed26619eed1) you specify, determines the gloss.

   **Roughness:** For vignettes that use reflection, you can set this material's roughness.

   ** Material:** Choose a material from the list.

   **Sharpen:** Choose the type of sharpening to apply.

   **Opacity:** Indicate to what degree the decal should obscure the texture beneath it. 

1. Click the **[!UICONTROL Image]** tab to change the file used for the decal, and to adjust its resolution, anchor point, thickness, base color, or opacity.

   **File/URL:** Specify the full path to the image file for this decal.

   **Resolution:** Specify the image resolution in pixels per inch.

   ** Anchor Point:** Specify where this decal attaches to the object beneath it. To anchor it at its center, click **[!UICONTROL Center]**.

   **Thickness:** Generally, decals have no thickness, but you can indicate a thickness if appropriate.

   **Base Color:** Click the color box to [choose a color](../../../c-vat-rend-pg/c-vat-rend-obj/t-vat-rend-solid-color.md#task-e051bda9851e4c6fb7e33a38b6e47f0d). To return to the original color, click ![](assets/back_arrow.png).

   **Opacity**: Indicate to what degree the base color should obscure the texture beneath it.

   **Gloss Map File:** If you have created a file that specifies an alpha channel for independent areas to receive gloss (for example, for a metallic thread or satin section of a decal), specify that file here. Gloss settings are applied to the alpha channel of the decal image only. 

1. To see information about the current decal file, click the **[!UICONTROL File Info]** tab.
1. Click the **[!UICONTROL Apply]** tab to change the angle or position of the decal. This is the same as [using the [!DNL Decal] tool](../../../c-vat-rend-pg/c-vat-rend-tools/c-vat-decal-tool.md#concept-359ac0b7c4ee42ddb104f9d12c01d596).
1. Click the **[!UICONTROL Render]** tab to [change [!DNL Sharpen] and [!DNL Illumination] settings](../../../c-vat-rend-pg/c-vat-work-text/c-vat-text-mat-prop/c-vat-text-mat-prop.md#concept-56e919cfd48748169dc2f011aa95c5fd) for the decal.

>[!MORELIKETHIS]
>
>* [Applying a Decal](../../../c-vat-rend-pg/c-vat-rend-obj/c-vat-decals/t-vat-app-decal.md#task-16ff67be05f84b06b4c0caf73ff01f83)
>* [The Decal Tool](../../../c-vat-rend-pg/c-vat-rend-tools/c-vat-decal-tool.md#concept-359ac0b7c4ee42ddb104f9d12c01d596)
