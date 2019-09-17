---
description: If you have saved materials for the current vignette, you can render and save one image file for each object/material combination in the palette.
seo-description: If you have saved materials for the current vignette, you can render and save one image file for each object/material combination in the palette.
seo-title: Batch Rendering to IPS
solution: Experience Manager
title: Batch Rendering to IPS
topic: Scene7 Image Authoring
uuid: 81cc1c9d-0ea9-41db-8bdd-4c3fc2f949fd
---

# Batch Rendering to IPS{#batch-rendering-to-ips}

If you have saved materials for the current vignette, you can render and save one image file for each object/material combination in the palette.

If you are using the [!DNL Image Production System], and have [configured the IPS settings](../../c-vat-img-auth-opt/t-vat-config-ips-settings.md#task-a58a6c7d64a3442c9c7e4f62ef99f9a8), you can batch-render the resulting rendered images directly to the IPS.

When you upload a render set, [!DNL Image Authoring] creates a separate swatch for each color or texture you use in this batch-render process and adds those items to IPS as separate files. The entire set of images is stored as a render set within IPS. If the materials already exist in IPS, [!DNL Image Authoring] won't upload them.

**To Batch Render to IPS:** 

1. [Save](../../c-vat-rend-pg/c-vat-rend-tools/t-vat-saved-mat-tool/t-vat-saved-mat-tool.md#task-2f7dd900c44e42f4a8e7f41a3003e2fa) each object/material combination you want to render.
1. Click the **[!UICONTROL Saved Materials]** tool ![](assets/saved_mat.png).
1. Click **[!UICONTROL Batch Render]**.
1. In the [!DNL Batch Render Setup] dialog box, choose **[!UICONTROL Index File]** or **[!UICONTROL Long File Names]**.

   ** Index File:** At the end of the process, the rendered images have file names that consist of the base file name followed by an underscore and a sequential number. Each file name uses the appropriate file extension for the file type you choose.

   For example, if you specify the file type [!DNL .JPG] and the base file name "bedroom," the resulting files would have the names [!DNL bedroom_0.jpg], [!DNL bedroom_1.jpg], and so on.

   **Long File Names**: At the end of the process, the rendered images have file names that consist of the base file name followed by an underscore and the name of the applied materials in that rendering. Each file name uses the appropriate file extension for the file type you choose.

   For example, if you specify the file type [!DNL .JPG] and the base file name "bedroom," the resulting files would have the names [!DNL bedroom_blue_oak_checker_maple.jpg], [!DNL bedroom_red_oak_checker_maple.jpg], and so on.

   In both cases, the elements of the output file names are separated by the [separator token character](../../c-vat-rend-pg/c-vat-abt-rend-pg/c-vat-rend-pg-pref.md#concept-158b19aeeda74bb28fcac3b684ca1efc) specified on the [!DNL Render] tab of the [!DNL Preferences] dialog box. 

1. Check the **[!UICONTROL Save to IPS]** checkbox.

   This checkbox does not appear if you do not have IPS. 

1. Click **[!UICONTROL OK]**.

   The [ [!DNL IPS Export]](../../c-vat-vign-img-rend/t-vat-exp-ips.md#task-a3367d2830a544e99bca84633b7fee7d) dialog box appears. You can [set preferences](../../c-vat-img-auth-opt/t-vat-config-ips-settings.md#task-a58a6c7d64a3442c9c7e4f62ef99f9a8) that let you specify a pathname to an IPS folder and continue using [!DNL Image Authoring] while the files are uploaded to IPS.

   You can see each combination rendered on screen as the batch process proceeds. Click **[!UICONTROL Cancel]** (in the lower left corner of the window) to interrupt the process. You can monitor the progress bar in the lower right. 

