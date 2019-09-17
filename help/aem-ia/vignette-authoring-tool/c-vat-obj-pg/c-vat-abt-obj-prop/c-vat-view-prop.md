---
description: To see the View Properties dialog box, Ctrl-click in the toolbar from any page, or right-click the view name in the Object Explorer and choose Properties.
seo-description: To see the View Properties dialog box, Ctrl-click in the toolbar from any page, or right-click the view name in the Object Explorer and choose Properties.
seo-title: View Properties
solution: Experience Manager
title: View Properties
topic: Scene7 Image Authoring
uuid: 75958816-a9ce-4085-9f21-2f8ed44e782a
---

# View Properties{#view-properties}

To see the View Properties dialog box, Ctrl-click in the toolbar from any page, or right-click the view name in the Object Explorer and choose Properties.

 The [!DNL View Properties] dialog box has the following tabs.

## General {#section-f1526af1c0d74cf789147e47c1e22eaa}

** Name:** The name you provided when you created the view. You can change this at any time.

**View Image Size:** The original size of the image in pixels.

** Default Print Resolution:** The default pixels per inch when the image is printed.

**Default Texture Resolution:** Unlike a normal resolution setting of pixels per inch on screen, the default resolution sets the [number of pixels in one inch of the texture image](../../c-vat-gs/c-vat-abt-res.md#concept-b15c68590bff427599cb0ee380606a0c). In order to set this option properly, you must know the actual dimensions of the texture.

For example, if the image is 80 pixels wide, and it represents an 8"x8" swatch, then 80 pixels is equal to 8 inches in real life. Therefore, you would set Resolution to 10, because 10 pixels represent each inch of the swatch.

**Actual Range of Texture Resolutions:** This is based on textures you have applied on the [!DNL Render] page and cannot be changed.

**Common Render Settings:** The vignette render settings that are used in the [ [!DNL Render] page](../../c-vat-rend-pg/c-vat-work-text/c-vat-text-mat-prop/c-vat-render.md#concept-c2c8c5e35662417c9508f85b52b24960).

** Action:**

* **Load From File:** Loads another original image file. The image file replaces the view image in your vignette. Be sure that the replacement image is the same size as the current image. 
* **Show:** Displays the original image file on which you based this vignette. All vignette properties (such as defined objects, masks, and so forth) are unavailable in this window. Choose the vignette from the Window menu to see the authored vignette again.

## Illumination {#section-dcba91ec0a314f709f738036713405b7}

Lets you show, [load](../../c-vat-work-illum-pg/c-vat-work-illum-maps/t-vat-imp-illum-map.md#task-2171a079ad2b45ada70487cbbcff5d89), [delete](../../c-vat-work-illum-pg/c-vat-work-illum-maps/t-vat-reset-illum-map.md#task-4b9217cc2a014379a7866e8187c3036b), and export three possible [!DNL Illumination Maps].

[!DNL Illumination Maps] help to determine the glossiness of objects when you render them. The [!DNL Illumination Maps] are not active until you check them. You can copy the default illumination map ( Map A), then set a different Gloss value for Map B and C, so you can apply higher or lower gloss when you render.

** Gloss Effects:** Check this box to blend the settings for these maps to achieve the best result. If you check this box and you have only one [!DNL Illumination Map], [!DNL Image Authoring] extrapolates above and below that map's Gloss setting to achieve good gloss results. If you don't check this box, [!DNL Image Authoring] uses only the [ [!DNL Illumination Map] you specify when you render the image](../../c-vat-rend-pg/c-vat-abt-rend-pg/c-vat-rend-pg-opt.md#concept-435a087c42b344b5b66ef946e4c825f7).

**Use Alternative Shader:** Check this box for apparel and upholstery vignettes if you want to fine-tune shading for very saturated or very light colors or textures. This enables the [!DNL Shader] tab on the [!DNL Material Property] dialog box on the [!DNL Render] page. The alternative shader considers gloss, but not material type.

**Action:**

* **Extract from Current View:** Creates an illumination map based on the current view. 
* **Load from File:** Loads a grayscale image as the illumination map. 
* **Set All Pixels to Neutral Gray:** Neutralizes the illumination map. 
* **Export to File:** Exports the illumination map. 
* ** Delete:** Removes the illumination map.

## Camera {#section-971c17a4eb0a4a5ead2429201529f57c}

Provides information about the [camera you set](../../c-vat-3d-mod-pg/c-vat-create-geo/t-vat-set-block.md#task-383646d12ec14e84b47d75fad4489175) on the [ [!DNL 3D Modeling] page](../../c-vat-3d-mod-pg/c-vat-abt-3d-mod-pg/c-vat-abt-3d-mod-pg.md#concept-93553c563c534d839a5cf0f2aafa70ee). If this tab doesn't appear, you haven't set the camera yet.

## Edges {#section-55153a6500a94f7694b6e4248d173cc9}

Shows you how many edges are stored in your vignette, and lets you delete them if they are making the vignette too large. This tab is available only if you have used the [ [!DNL Extract Edges from Image]](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-edge-recog-masks.md#task-4fe94280df4848baae7f6c417890022a) feature on the [!DNL Mask] or [!DNL Sketch] page and saved the edge data. 
