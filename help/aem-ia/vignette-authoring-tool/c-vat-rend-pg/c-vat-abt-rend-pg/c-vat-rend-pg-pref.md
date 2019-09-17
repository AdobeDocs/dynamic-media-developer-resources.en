---
description: The Render page preferences (available from Preferences on the Edit menu) affect rendering for the entire image.
seo-description: The Render page preferences (available from Preferences on the Edit menu) affect rendering for the entire image.
seo-title: Render Page Preferences
solution: Experience Manager
title: Render Page Preferences
topic: Scene7 Image Authoring
uuid: 16118794-d2ef-45e6-a350-638a692c360a
---

# Render Page Preferences{#render-page-preferences}

The Render page preferences (available from Preferences on the Edit menu) affect rendering for the entire image.

**Show Overlap Objects When Renderer is Reset:** When the renderer is reset, all overlapping objects are rendered. If you have a vignette with many overlapping objects, you should remove the check for this option.

**Use Less Memory for Rendering:** Allocates less memory to the rendering process, which may make the rendering slower.

**Material File Download/Upload Timeout:** Indicates the number of seconds that [!DNL Image Authoring] continues to try to connect to the [!DNL Image Production System] server. If it cannot connect within the specified number of seconds, an error displays.

**Separator Token for Batch Render Files:** Specifies the character that separates each element of the filenames created during [batch rendering](../../c-vat-rend-pg/c-vat-rend-obj/t-vat-batch-rend.md#task-5d1986172ea0426892163cfa54a142a7).

**Auto-reset Renderer After Vignette Edits:** You can reset all options on the [!DNL Render] page immediately or each time you edit your vignette and return to the [!DNL Render] page. You must apply a new material to see the results of your changes. If you set this option to Never, the previous rendering results display, which may be misleading.

**Number of Items in Material History:** Indicates the largest number of items that [!DNL Image Authoring] should keep in the [!DNL Material History] list. When this limit is reached, the oldest material is discarded and the newest one is added. Click **[!UICONTROL Clear History]** to clear out this list.

**Obtain Initial Texture/Decal Resolution From:** Specifies how [!DNL Image Authoring] determines the resolution for textures and decals, and whether it prompts you for this information. You can specify that the prompt appear in all cases, whether [!DNL Image Authoring] finds the resolution information in the material template or the print resolution saved with the image or not, or any combination of these options. If you choose a prompt option, you can bypass the prompt by holding down the Shift key when you click **[!UICONTROL Open]** to add a texture on the [!DNL Render] page. If you do this, you see the [ [!DNL Texture Materials Property] dialog box](../../c-vat-rend-pg/c-vat-work-text/c-vat-text-mat-prop/c-vat-text-mat-prop.md#concept-56e919cfd48748169dc2f011aa95c5fd) instead, where you can set the resolution and other properties.

**Material Drag & Drop Behavior:** Indicates the way [!DNL Image Authoring] responds when you [drag and drop a material](../../c-vat-rend-pg/c-vat-rend-obj/t-vat-drag-text.md#task-cad3f740e6194876b25ca2704630aeec) from the [!DNL Image Production System], or from Windows Explorer.

* **Select Object at Drop Location:** Applies the material to the object you click when you drop the material in [!DNL Image Authoring]. You see a menu of items you can choose, including the parent group and any sub-groups. If you don't check this option, [!DNL Image Authoring] applies the material to the object or group selected in the [ [!DNL Select Object] box](../../c-vat-gs/c-vat-sel-obj/c-vat-sel-object-box.md#concept-d127c6efaabd436a96c02f36a7bce6ac). 

* **Save Material to Vignette:** Adds the material to your [!DNL Saved Materials] list when you drop it. 

* **Render After Drop:** Renders the object affected by the new material as soon as you drop it in your vignette.

To save sets of rendering settings for textures, colors, and window coverings, use [material templates](../../c-vat-rend-pg/c-vat-work-text/t-vat-mat-templ.md#task-8f5d1c397c19469d9ab4fafd2312db83). 
