---
description: You can export (save) objects to Photoshop.
seo-description: You can export (save) objects to Photoshop.
seo-title: Exporting to Photoshop
solution: Experience Manager
title: Exporting to Photoshop
topic: Scene7 Image Authoring
uuid: 11243830-21d4-4f12-8c61-56ac4689e82a
---

# Exporting to Photoshop{#exporting-to-photoshop}

You can export (save) objects to Photoshop.

The exported objects become layers in the resulting PSD file. Renderable overlap objects result in one layer per illumination map, forming a layer set. Any vector paths you have saved with an image is maintained.

**To Export a Vignette in PSD Format:** 

1. On the [!DNL Object] page, right-click the vignette in the [!DNL Object Hierarchy].
1. Click **[!UICONTROL Export .PSD File]**.
1. Enter a name in the [!DNL File] name box.
1. Click **[!UICONTROL Save]**.
1. Specify whether to export the view image or an illumination map.
1. Specify the [print resolution for the vignette](../../c-vat-gs/c-vat-abt-res.md#concept-b15c68590bff427599cb0ee380606a0c), whether you want to use RLE compression (for smaller file size), and how to deal with [color management](../../c-vat-gs/c-vat-abt-color-mgmt/c-vat-abt-color-mgmt.md#concept-2a2d355fd8e841ca95a926397aed4cab) settings.
You can also save a vignette as a layered PSD ( [!DNL Photoshop]) file by [batch-rendering](../../c-vat-rend-pg/c-vat-rend-obj/t-vat-psd-files.md#task-a85b96fead60418a8b2cad9c10f884e4) the images. You can export a flat image using the [ [!DNL File] menu [!DNL Export] option](../../c-vat-vign-img-rend/t-vat-exp-vign-img-file.md#task-18c83bf6c1ff4c879fc87939835c3e44). You can re-import [masks](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-imp-mask.md#task-48b7eadbdd7a4b23a3b34d14b59ce787), [illumination maps](../../c-vat-work-illum-pg/c-vat-work-illum-maps/t-vat-imp-illum-map.md#task-2171a079ad2b45ada70487cbbcff5d89), [drop shadows](../../c-vat-obj-pg/c-vat-work-obj/c-vat-drop-shadows.md#concept-6f10112a1e954bc5a0d29c116891fb6e), and [view images](../../c-vat-gs/c-vat-work-ps/c-vat-imp-ps/c-vat-imp-ps.md#concept-ea136cbe07dd4ce5ba5e169bf413583a). [!DNL Image Authoring] reassigns them appropriately in the [!DNL Object Hierarchy], as long as you don't change the names of their layers in [!DNL Photoshop]. 