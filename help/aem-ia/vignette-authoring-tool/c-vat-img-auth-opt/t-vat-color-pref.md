---
description: The color settings determine the default color management behavior of Image Authoring.
seo-description: The color settings determine the default color management behavior of Image Authoring.
seo-title: Setting Color Preferences
solution: Experience Manager
title: Setting Color Preferences
topic: Scene7 Image Authoring
uuid: a7030bea-249c-4f24-855a-0b655de02cec
index: y
internal: n
snippet: y
---

# Setting Color Preferences{#setting-color-preferences}

The color settings determine the default color management behavior of Image Authoring.

You can set a default ICC color profile for working in [!DNL Image Authoring] (the working color space), and for different types of images you import.

The [!DNL Monitor Profile] determines how colors appear on your monitor, it does not change the color information in an image. When you [export a vignette to an image format](../c-vat-vign-img-rend/t-vat-exp-vign-img-file.md#task-18c83bf6c1ff4c879fc87939835c3e44), the working color space is used to generate the exported image and you can embed that color space as a color profile.

Import preferences let you change the color space for images you open in [!DNL Image Authoring]. You specify whether images with mismatched or missing color profiles are automatically converted to your default or not.

You can check various color spaces on your monitor before choosing these settings by [using the [!DNL Proof Colors] feature.](../c-vat-gs/c-vat-abt-color-mgmt/c-vat-abt-color-mgmt.md#concept-2a2d355fd8e841ca95a926397aed4cab)

**To Change Color Preferences:** 

1. On the [!DNL Edit] menu, select **[!UICONTROL Preferences]**.
1. In the [!DNL Color] tab, set the following:

    * **Working (RGB):** Choose a working color space. Newly created vignettes default to this color profile. All RGB color spaces found in your [!DNL system32\spool\drivers\color] directory appear in this list. 
    
    * ** Import (RGB):** Choose a default color space for RGB images that you open in [!DNL Image Authoring]. All RGB color spaces found in your [!DNL system32\spool\drivers\color] directory appear in this list. 
    
    * **Import (CMYK): **Choose a default color space for CMYK images that you open in [!DNL Image Authoring]. All CMYK color spaces found in your [!DNL system32\spool\drivers\color] directory appear in this list. 
    
    * **Import (Gray):** Choose a default color space for grayscale images that you open in [!DNL Image Authoring]. All grayscale color spaces found in your [!DNL system32\spool\drivers\color] directory appear in this list. 
    
    * **When Importing Images Without Profiles:** Specify whether to automatically convert images with no color profiles to the appropriate default color space specified above. If you don't want to convert images automatically, you can have [!DNL Image Authoring] prompt you for each image that has no color profile, or you can choose to ignore color management for all such images. 
    
    * **When Importing Images with Mismatched Profiles:** Specify whether to automatically convert images whose color profiles do not match the current working color space (specified above) to use the appropriate default color space (also specified above). If you don't want to convert images automatically, you can have [!DNL Image Authoring] prompt you for each of these images, or you can choose to ignore embedded color information. 
    
    * **Monitor Profile:** If you have calibrated your monitor and have a color profile for it, choose it from this list.

1. Click **[!UICONTROL OK]**.
