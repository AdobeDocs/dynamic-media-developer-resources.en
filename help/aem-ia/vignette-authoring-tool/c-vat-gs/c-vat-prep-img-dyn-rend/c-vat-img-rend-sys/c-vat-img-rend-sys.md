---
description: You use the Vignette Update tool to prepare vignettes for deployment to the Image Rendering System.
seo-description: You use the Vignette Update tool to prepare vignettes for deployment to the Image Rendering System.
seo-title: Sending Images to the Image Rendering System
solution: Experience Manager
title: Sending Images to the Image Rendering System
topic: Scene7 Image Authoring
uuid: 2f24c05d-e7ba-426e-8e0e-68ea0a1d5741
index: y
internal: n
snippet: y
---

# Sending Images to the Image Rendering System{#sending-images-to-the-image-rendering-system}

You use the Vignette Update tool to prepare vignettes for deployment to the Image Rendering System.

Follow these guidelines when you use the [!DNL Vignette Update] tool:

* Find out the size that will be used for the vignette on the website. If the vignette is displayed at more than one size, go through the [ [!DNL Vignette Update] tool ](../../../c-vat-gs/c-vat-prep-img-dyn-rend/c-vat-img-rend-sys/c-vat-abt-vign-update-tool.md#concept-61c09096c9384766b30097c814780780)once for each size, entering each image width once when prompted. If vignette is to be displayed at multiple sizes and [!DNL Image Rendering] is version 3.7.1 or higher, we recommend the [!DNL Output Vignette Type] be set to [!DNL Pyramid]. This typically gives better rendering results. 

* You may find it necessary to change the vignette's version to match the version of your server rendering software, because the current version of [!DNL Image Authoring] may use a different vignette version than the one [!DNL Image Rendering] is expecting. For example, [!DNL Image Authoring] (Infinite Imaging Software) 2.0.4 saves vignettes as version 51, whereas [!DNL Image Rendering] 3.0.7 is expecting vignettes as version 50. 

* With the latest [ [!DNL Vignette Update] tool](../../../c-vat-gs/c-vat-prep-img-dyn-rend/c-vat-img-rend-sys/c-vat-abt-vign-update-tool.md#concept-61c09096c9384766b30097c814780780), file name templates can be used. This is a new field where the user can set what the file name output will be. Make sure that the same naming convention is what the Web developers are expecting. 
* Image map output from the [ [!DNL Vignette Update] tool](../../../c-vat-gs/c-vat-prep-img-dyn-rend/c-vat-img-rend-sys/c-vat-abt-vign-update-tool.md#concept-61c09096c9384766b30097c814780780) has been removed. If you need image map coordinates for your vignette, then you need to export them from [!DNL Image Authoring].

