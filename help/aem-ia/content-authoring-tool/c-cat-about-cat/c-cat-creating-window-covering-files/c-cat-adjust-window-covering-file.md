---
description: You can use the Content Authoring tool to adjust the window covering settings.
seo-description: You can use the Content Authoring tool to adjust the window covering settings.
seo-title: Adjusting the Window Covering File
solution: Experience Manager
title: Adjusting the Window Covering File
topic: Scene7 Image Authoring
uuid: fb72d09d-9c7b-4b30-831f-16e1d0fa2f5f
---

# Adjusting the Window Covering File{#adjusting-the-window-covering-file}

You can use the Content Authoring tool to adjust the window covering settings.

## Illumination {#section-1fc583c2b15c4d05b6bff2226b0cb79f}

** Load Image:** Click this button to import a different illumination map file.

**Resolution:** How many pixels in the window covering correspond to an inch in world space. There are two ways to determine this resolution:

You can measure the original window covering and measure the image onscreen at full-size to determine the number of pixels in its width and height, then divide the pixels by the real-life size to find the pixels per inch.

If you know that the window covering was scaled at 300 dpi and you scaled at 4.5, you can divide 300 by 4.5 to get the same information. If you plan to scale many window coverings, you may want to set your scale factor so you always end up with the same resolution.

** Gloss:** Specify the percentage of gloss this window covering will have, independent of any texture applied to it.

**Thickness:** Specify the thickness of this window covering. This determines drop shadows displayed by the window covering when you apply it in [!DNL Image Authoring].

## Mask {#section-9ca02867ff654c2fada2654fa32d45b0}

**Load Image:** Click this button to import a different mask file.

## Opacity {#section-f5052cf316854f509547bb031cbfbfab}

** Load Image:** Click this button to import any file you created in a photo-editing program to specify the opacity of the window covering (that is, its illumination when backlit), so that transparency is convincing when folds of the window covering overlap.

## UV Data {#section-1e708d31d560433384881a5a09984bde}

**Load Image:** Click this button to import flowlines you previously exported from [!DNL Image Authoring] as a [!DNL .vnf] file.

The other settings on this tab are inherited from the flowline data you import.

## Texture {#section-8a04fb7f6ac5476e90686fc7f673b324}

The settings on this tab are inherited from the settings on the [!DNL Illumination] tab.

**Size:** The width and height of the window covering in inches.

**Origin:** The point at which the upper left corner of the first full texture tile appears on the window covering. The origin value is in inches relative to the top, left corner.

**Resolution:** How many pixels in the window covering correspond to an inch in world space. 
