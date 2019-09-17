---
description: Use the Add Feature tool to create sketch lines that define the features of your object.
seo-description: Use the Add Feature tool to create sketch lines that define the features of your object.
seo-title: The Add Feature Tool
solution: Experience Manager
title: The Add Feature Tool
topic: Scene7 Image Authoring
uuid: bc4ae57f-b2f3-4ae4-8af6-2b7f20aaa515
---

# The Add Feature Tool{#the-add-feature-tool}

Use the Add Feature tool to create sketch lines that define the features of your object.

The [!DNL Add Feature] tool has the following options:

* **Feature Type:** Determines the type of sketch line you are adding. Each [feature type](../../c-vat-work-sketch-pg/r-vat-create-sketch-feat/r-vat-create-sketch-feat.md#reference-b7085135ac07423293bf9014bfebf461) renders differently.

Use the [!DNL Pen] tab to [draw features](../../c-vat-work-sketch-pg/r-vat-create-sketch-feat/r-vat-create-sketch-feat.md#reference-b7085135ac07423293bf9014bfebf461). Click to start adding vertexes and double-click to finish the feature line. Press the Esc key to remove all vertexes.

Use the [!DNL Pencil] tab to adjust smoothing:

* **Feature Smoothing:** Determines how closely the feature follows the exact trajectory of your cursor. Move the slider between Less and More to adjust for noise and jerkiness. You can change the tracking accuracy before you draw an object. 
* **Snap to Mask Edges:** Determines whether the feature you are drawing snaps to the defined mask for the current object. This option is most useful for [!DNL Horizon Edge] and [!DNL Hidden Area] features. You can set [!DNL Snap to mask edges] to do so Always, or to snap only when you hold down the Shift key (the default). 

* **Snap Radius:** Specifies how close (in pixels) the cursor must be to the defined mask edge in order to snap to it.

Use the [!DNL Edge] tab to [define the edges of a feature](../../c-vat-work-sketch-pg/r-vat-create-sketch-feat/t-vat-edge-recog-sketch.md#task-ba7dbbb14c084f7dbfe416f5aa5aff2b):

* **Sensitivity:** Adjusts the edge definition. Lowering the sensitivity causes only the highest-contrast areas to be defined as edges. Raising it causes more edges to appear, but they may interfere with the true edges of objects. 
* **Display:** Adjusts the appearance of edges from opaque to transparent. 
* **Recalc:** Displays the [!DNL Extract Edges from Image] dialog box, where you can set options for [defining default edges](../../c-vat-work-sketch-pg/r-vat-create-sketch-feat/t-vat-edge-recog-sketch.md#task-ba7dbbb14c084f7dbfe416f5aa5aff2b).

>[!MORE_LIKE_THIS]
>
>* [About the Sketch Page](../../c-vat-work-sketch-pg/c-vat-abt-sketch-pg/c-vat-abt-sketch-pg.md#concept-7e6bb452319c45ea9663920dd2f06d85)
>* [Creating a Feature](../../c-vat-work-sketch-pg/r-vat-create-sketch-feat/t-vat-create-feat.md#task-c4fd7e414a9445a49b4c2a3cf7425481)
