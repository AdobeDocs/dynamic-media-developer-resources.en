---
description: The Flowline page preferences (available from Preferences on the Edit menu) affect flowlines for the entire image.
seo-description: The Flowline page preferences (available from Preferences on the Edit menu) affect flowlines for the entire image.
seo-title: Flowline Page Preferences
solution: Experience Manager
title: Flowline Page Preferences
topic: Scene7 Image Authoring
uuid: ebd30efe-c12f-4114-8883-19b4294ce7bf
---

# Flowline Page Preferences{#flowline-page-preferences}

The Flowline page preferences (available from Preferences on the Edit menu) affect flowlines for the entire image.

There are two sets of preferences:

**Redraw the Preview Texture During Vertex Moves:** This setting provides live feedback when you adjust flowlines. It is unchecked by default.

**Advanced:** Click this button to see the advanced [!DNL Flowline] page preferences. Most of the time, you don't need to change them. However, if you have very high resolution apparel images or very low resolution images, you may need to change some of them.

* **Meshing Preferences**

**Show Mesh:** Displays a cross-hatched wire pattern for the [!DNL Flowline Mesh], instead of the flowline outline and flowlines (or preview material). This setting is unchecked by default.

[!DNL Map] represents the quality of the [!DNL Flowline Mesh] after you've finished editing it. [!DNL Static] represents the changes in texture shown when you let go of the [!DNL Flowline Mesh]. [!DNL Moving] shows changes in texture as you adjust the [!DNL Flowline Mesh].

* **Default Flowline Spacing**

Specify the initial mesh for new flowline objects. By default, this is 2 by 2, which results in a bounding box around the object (two vertical lines and two horizontal lines). The number of lines is based on the spacing in pixels that you specify here. The smaller the value, the greater the number of flowlines in the initial mesh.

* **Line Accuracy**

Flowlines are a vector overlay on top of your bitmapped image. This setting determines how the flowlines line up with the pixels in the view image. For low resolution images, adjusting this setting can make a difference in the accuracy of the flowlines.

* **Lines Defaults Preferences**

These settings take effect when you add a line with the [ [!DNL Flowline Mesh] tool](../../c-vat-flow-pg/c-vat-use-flow-tools/c-vat-mesh-tool.md#concept-a3383512cf714c58b2afc41a9ccb261b).

**Line Tension:** Sets default value for the [ [!DNL Tension] slider](/help/aem-ia/vignette-authoring-tool/c-vat-flow-pg/c-vat-create-flow/c-vat-create-flow.md).

** Line Depth:** Sets default value for the [ [!DNL Depth] slider](../../c-vat-flow-pg/c-vat-flow-mesh-tech/t-vat-depth-text.md#task-18d316e8b07d4f5a859589ae96f97693).

**Texture Tension:** Affects how textures bend to adapt to the [flowline bends](../../c-vat-flow-pg/c-vat-create-flow/t-vat-contour-flow-mesh.md#task-1d891b7540014e5c823278c5e4d69dbb). Higher numbers make the texture smoother at deep bends.

* **Vertex Defaults Preferences**

These settings take effect when you add a vertex with the [!DNL Mesh] tool. They are the same as the [!DNL Lines Defaults] preferences, except they affect vertexes instead of lines. 
