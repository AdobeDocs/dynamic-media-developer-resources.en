---
description: You can change information about the window covering you apply.
seo-description: You can change information about the window covering you apply.
seo-title: Changing Window Covering Material Properties
solution: Experience Manager
title: Changing Window Covering Material Properties
topic: Scene7 Image Authoring
uuid: ecb95614-e758-4fe0-a82c-44896a8a55f9
---

# Changing Window Covering Material Properties{#changing-window-covering-material-properties}

You can change information about the window covering you apply.

 ** To Change the Properties for a Window Covering:** 

1. Right-click the object to which you applied the window covering and choose **[!UICONTROL Material Properties]**.
1. In the [!DNL Window Coverings Material Properties] dialog box, click the **[!UICONTROL General]** tab to change information about the window covering.

   **Name/ID:** This is the name that appears in [ [!DNL Material History]](../../../c-vat-rend-pg/c-vat-rend-tools/t-vat-mat-hist-tool.md#task-95e1391588974719bbf93850448d547b), [ [!DNL Favorite Materials]](../../../c-vat-rend-pg/c-vat-rend-tools/c-vat-fav-mat-tool/t-vat-fav-mat-list.md#task-488e210530c24f6bbf7b37d0b6109b61), and [ [!DNL Saved Materials]](../../../c-vat-rend-pg/c-vat-rend-tools/t-vat-saved-mat-tool/t-vat-saved-mat-tool.md#task-2f7dd900c44e42f4a8e7f41a3003e2fa).

   **Colorize:** Check this box to add a color to the applied texture. Click the color box to [choose a color](../../../c-vat-rend-pg/c-vat-rend-obj/t-vat-rend-solid-color.md#task-e051bda9851e4c6fb7e33a38b6e47f0d).

   **Preferred Illum Map:** This setting does not affect window coverings.

   ** [Gloss](../../../r-vat-glossary/c-vat-gloss.md#concept-c935eeb0b63442368231fb26b5a58f50):** Specify the percentage of shininess for this image. Window coverings have a single [!DNL Illumination Map], and are not affected by the active [ [!DNL Illumination Maps] or gloss settings in the [!DNL View Properties] dialog box](../../../c-vat-obj-pg/c-vat-abt-obj-prop/c-vat-view-prop.md#concept-8a396f7b144c46c4806c8ed26619eed1).

   ** Roughness:** For vignettes that use reflection, you can set this material's roughness.

   **Material:** Choose a material from the list.

   **Opacity:** Indicate to what degree the window covering should obscure the objects beneath it. 

1. Click the **[!UICONTROL Style File]** tab to change the file used for the window covering.

   **File/URL:** Specify the full path to the [!DNL .vnw] file for this window covering.

   **Resolution:** Displays the image resolution in pixels per inch. This setting is determined by the [!DNL .vnw] file, you cannot change it here.

   **Type:** Displays the type of window covering this is (short drape, blinds, and so forth). This setting is determined by the [!DNL .vnw] file, you cannot change it here. 

1. Click the **[!UICONTROL Texture]** tab to change the texture file used for the window covering, and to adjust its resolution, anchor point, repeat type, base color, or gloss.

   **File/URL:** Specify the full path to the image file for this texture.

   **Resolution:** Specify the image resolution in pixels per inch.

   **Anchor Point:** Specify where this texture attaches to the window covering. To anchor it at its center, click **[!UICONTROL Center]**.

   **Repeat type:** Choose a [repeat type](../../../c-vat-rend-pg/c-vat-work-text/c-vat-text-mat-prop/c-vat-text-mat-prop.md#concept-56e919cfd48748169dc2f011aa95c5fd) for this texture.

   ** Base Color:** Click the color box to [choose a color](../../../c-vat-rend-pg/c-vat-rend-obj/t-vat-rend-solid-color.md#task-e051bda9851e4c6fb7e33a38b6e47f0d).

   **Apply to:** Specify the [origin](../../../c-vat-rend-pg/c-vat-work-text/c-vat-abt-origin.md#concept-643d030b62fd42a5bf3ce4e4ab9a3a47) for this texture.

   **Gloss Map File:** If you have created a file that specifies an alpha channel for independent areas to receive gloss (for example, for a metallic thread or satin section of a decal), specify that file here. [!DNL Gloss] settings are applied to the alpha channel of the window covering texture only. 

1. To see information about the current window covering file, click the [!DNL File Info] tab.
1. To apply sharpening or resampling, click the **[!UICONTROL Sharpen]** tab.
1. Click the **[!UICONTROL Render]** tab to [change [!DNL Sharpen] and [!DNL Illumination] settings](../../../c-vat-rend-pg/c-vat-work-text/c-vat-text-mat-prop/c-vat-text-mat-prop.md#concept-56e919cfd48748169dc2f011aa95c5fd) for the window covering.
