---
description: If you are using Photoshop, you can batch-render images as layered .psd files.
seo-description: If you are using Photoshop, you can batch-render images as layered .psd files.
seo-title: Batch Rendering PSD Files
solution: Experience Manager
title: Batch Rendering PSD Files
topic: Scene7 Image Authoring
uuid: fbba96c1-4a29-41fa-9bb1-df9a61b19976
---

# Batch Rendering PSD Files{#batch-rendering-psd-files}

If you are using Photoshop, you can batch-render images as layered .psd files.

This results in a [!DNL Photoshop] [!DNL .psd] file where each material is saved as a separate layer.

If the vignette uses an ICC color profile (for example, if you embedded such a profile in the image before authoring it in [!DNL Image Authoring]), this information is saved with the batch render using [!DNL Run Length Encoding] (which results in smaller files). The resulting PSD file displays the embedded profile information when you open it in [!DNL Photoshop].

To save a layered [!DNL Photoshop] [!DNL .psd] file to IPS: 

1. Save a texture to each object or group that becomes a layer.
1. Click the **[!UICONTROL Saved Materials]** tool ![](assets/saved_mat.png).
1. Click **[!UICONTROL Batch Render]**.
1. In the [!DNL Batch Render Setup] dialog box, choose **[!UICONTROL Layered File]**.
1. Click **[!UICONTROL OK]**.

   Set any options for the resulting [!DNL Photoshop] file, such as the resolution, compression, and color settings.

   You can see each combination rendered on screen as the batch process proceeds. Click **[!UICONTROL Cancel]** (in the lower left corner of the window) to interrupt the process. You can monitor the progress bar in the lower right. 

