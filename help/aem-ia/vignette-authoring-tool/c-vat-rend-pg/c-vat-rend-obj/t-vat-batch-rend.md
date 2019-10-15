---
description: If you have saved materials for the current vignette, you can render and save one vignette image file for each object or group/material combination in the palette.
seo-description: If you have saved materials for the current vignette, you can render and save one vignette image file for each object or group/material combination in the palette.
seo-title: Batch Rendering
solution: Experience Manager
title: Batch Rendering
topic: Scene7 Image Authoring
uuid: 55a4ad98-0a1c-4e3c-be5f-b833d239de49
---

# Batch Rendering{#batch-rendering}

If you have saved materials for the current vignette, you can render and save one vignette image file for each object or group/material combination in the palette.

 **To Batch Render the Vignette:** 

1. [Save](../../c-vat-rend-pg/c-vat-rend-tools/t-vat-saved-mat-tool/t-vat-saved-mat-tool.md#task-2f7dd900c44e42f4a8e7f41a3003e2fa) each object or group/material combination you want to render.
1. Click the **[!UICONTROL Saved Materials]** tool ![](assets/saved_mat.png).
1. Click **[!UICONTROL Batch Render]**.
1. In the [!DNL Batch Render Setup] dialog box, choose **[!UICONTROL Index File]** or **[!UICONTROL Long File Names]**, then click **[!UICONTROL OK]**.

   **Index File:** At the end of the process, the rendered images have file names that consist of the base file name followed by an underscore and a sequential number. Each file name uses the appropriate file extension for the file type you choose.

   For example, if you specify the file type [!DNL .JPG] and the base file name "bedroom," the resulting files would have the names [!DNL bedroom_0.jpg], [!DNL bedroom_1.jpg], and so on.

   With this option, a tab-delimited [!DNL .txt] file is saved, listing the saved images and the textures applied to each object or group within each one.

   **Long File Names:** At the end of the process, the rendered images have file names that consist of the base file name followed by an underscore and the name of the applied materials in that rendering. Each file name uses the appropriate file extension for the file type you choose.

   For example, if you specify the file type [!DNL .JPG] and the base file name "bedroom," the resulting files would have the names [!DNL bedroom_blue_oak_checker_maple.jpg], [!DNL bedroom_red_oak_checker_maple.jpg], and so on.

   In both cases, the elements of the output file names are separated by the [separator token character](../../c-vat-rend-pg/c-vat-abt-rend-pg/c-vat-rend-pg-pref.md#concept-158b19aeeda74bb28fcac3b684ca1efc) specified on the [!DNL Render] tab of the [!DNL Preferences] dialog box.

   If you see the [!DNL Save to IPS] checkbox, leave it unchecked unless you are [exporting to IPS](../../c-vat-rend-pg/c-vat-rend-obj/t-vat-batch-rend-ips.md#task-f89e8d1a7bc54694b14173505641a0df). This checkbox does not appear if you do not have IPS. 

1. In the [!DNL Save As] dialog box, indicate a base name, file type, and location for the batched output and click **[!UICONTROL Save]**.
You can see each combination rendered onscreen as the batch process proceeds. Click **[!UICONTROL Cancel]** (in the lower left corner of the window) to interrupt the process. You can monitor the progress bar in the lower right.

You can open each of the resulting image files in [!DNL Photoshop] (or another image editing program). 
