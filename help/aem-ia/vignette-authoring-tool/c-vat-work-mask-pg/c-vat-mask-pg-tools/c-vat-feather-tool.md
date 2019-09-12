---
description: When you apply feathering, the mask edge spreads out from an existing tool, adding and subtracting at the same time to make a soft edge.
seo-description: When you apply feathering, the mask edge spreads out from an existing tool, adding and subtracting at the same time to make a soft edge.
seo-title: The Feather Tool
solution: Experience Manager
title: The Feather Tool
topic: Scene7 Image Authoring
uuid: 4ff5dacb-8e18-436d-880d-7f3702c7745d
index: y
internal: n
snippet: y
---

# The Feather Tool{#the-feather-tool}

When you apply feathering, the mask edge spreads out from an existing tool, adding and subtracting at the same time to make a soft edge.

Feathering affects the two adjacent masks, feathering the edges of both masks. You can apply feathering settings to the entire mask. Your [!DNL Feather] tool ![](assets/feather.png)settings remain in effect until you change them again.

The [!DNL Feather] tool has the following option:

* ** Radius:** By default, the [!DNL Feather] tool affects three pixels of the mask edge, but you can adjust the [!DNL Radius] slider to set this anywhere between one and ten pixels. 

* **Set to Optimum:** Sets the feather tool radius to match the blurriness of the mask to the underlying image edge. It assumes that the mask edge has not been previously softened. 
* ** Adaptive Feathering:** Use this option to make the sharpness or blurriness of the applied texture or color blend in with the underlying image. [!DNL Adaptive Feathering] calculates the feathering radius during the brush stroke. If you click **[!UICONTROL Apply]** to [!DNL Whole Mask], it calculates the radius based on the entire edge.

If you use [!DNL Adaptive Feathering], the softening effect is greatest where the underlying image is softest and least where the underlying image is sharpest. [!DNL Adaptive Feathering] never exceeds the current [!DNL Radius] setting. 
