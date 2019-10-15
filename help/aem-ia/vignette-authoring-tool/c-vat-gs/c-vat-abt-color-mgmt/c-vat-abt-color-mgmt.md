---
description: Image Authoring provides several color management features.
seo-description: Image Authoring provides several color management features.
seo-title: About Color Management
solution: Experience Manager
title: About Color Management
topic: Scene7 Image Authoring
uuid: 8554c8af-1b0d-41e6-a6d0-94e808e8dabe
---

# About Color Management{#about-color-management}

Image Authoring provides several color management features.

* **Working Color Space:**
You can set a [working color space for the current vignette](../../c-vat-gs/t-vat-create-vign.md#task-a51b7fb4cce14ea88279116b24cc98b4), and you can set a [default working color space for all vignettes](../../c-vat-img-auth-opt/t-vat-color-pref.md#task-b73fd4722e9247e8bce1f5a70518c33d).

  Changing the color space does not change any color information in your vignette, but it does change the way that colors appear on your monitor. This setting affects the current vignette only and is saved with the vignette. 

* **Export Color Space**
When you [export a vignette to the PNG, TIF, or JPEG format](../../c-vat-vign-img-rend/t-vat-exp-vign-img-file.md#task-18c83bf6c1ff4c879fc87939835c3e44), you can specify whether to use the working color space or a different color space. For RGB, you can use PNG, JPG, and TIF files with color profiles. For CMYK, you can use JPG and TIF files with color profiles.

  If you keep the current working color space, the RGB values for your system are used to generate the new image. If you convert to a different color space, the RGB values are different from the ones you see on your screen. They are based on the new color space. You can embed the color space in the image (or not). 

* **Color Conversion for New Images**
You can [set a default color space for new RGB, CMYK, and grayscale images that you open in [!DNL Image Authoring]](../../c-vat-img-auth-opt/t-vat-color-pref.md#task-b73fd4722e9247e8bce1f5a70518c33d). You can specify whether all such images should use your defaults, whether to ignore color management for images whose color profiles are missing or mismatched, or whether [!DNL Image Authoring] should prompt you for each one. 

* **Color Proofing**
You can test color profiles with specific images in [!DNL Image Authoring]. You may want to do this before setting a working color space or import defaults. Color proofing is a two-step process.

