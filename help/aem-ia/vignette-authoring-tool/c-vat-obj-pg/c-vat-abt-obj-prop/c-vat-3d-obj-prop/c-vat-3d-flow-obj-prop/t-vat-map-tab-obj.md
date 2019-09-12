---
description: This tab lets you view information about the flowline data.
seo-description: This tab lets you view information about the flowline data.
seo-title: Map tab for objects
solution: Experience Manager
title: Map tab for objects
topic: Scene7 Image Authoring
uuid: 1803b3f6-2809-49a4-a409-a07356011d7d
index: y
internal: n
snippet: y
---

# Map tab for objects{#map-tab-for-objects}

This tab lets you view information about the flowline data.

 **Size:** The overall size of the texture space in inches. This value is the same as [ [!DNL Size on the Texture] tab](../../../../c-vat-obj-pg/c-vat-abt-obj-prop/c-vat-3d-obj-prop/c-vat-3d-flow-obj-prop/c-vat-text-tab-obj.md#concept-81d47c5bdaf64427a222acfee3e6d557), and the [ [!DNL Overall Size]](../../../../c-vat-flow-pg/c-vat-use-flow-tools/c-vat-text-tool.md#concept-e54c441b9ea644c0a496cc05c2465ea1) value in the [!DNL Texture] tool options. Set this value when importing a UV Map (see below).

**Resolution:** The resolution of the texture space (in pixels per inch). This value is normally calculated automatically, but may be specified when importing a UV Map (see below). This value is the same as [ [!DNL Optimal Resolution] on the [!DNL Texture] tab](../../../../c-vat-obj-pg/c-vat-abt-obj-prop/c-vat-3d-obj-prop/c-vat-3d-flow-obj-prop/c-vat-text-tab-obj.md#concept-81d47c5bdaf64427a222acfee3e6d557).

**Lock Width, Height Resolution Ratios:** When this box is checked, any changes you make to object size or resolution preserve the aspect ratio of the object.

**Action:** Click this button to see the following choices:

* **Generate Map Image from Map Data:** Choose this option if the map data is valid, but the map image is not, and if you need to preview the map properties. 
* **Export Flowlines:** Lets you save the [!DNL Flowline] data in a format that can be re-imported into [!DNL Image Authoring] for use in another image. 

* **Load Map Image from File:** You can import a UV map you created with 3D Studio MAX. The imported file must be in [!DNL .RLA] format. This feature is for advanced users only. See below. 

* **Copy Map Data from Another Object:** Lets you use the same imported UV map image for multiple objects. 
* **Import Flowlines (Fit to Mask):** Lets you import [!DNL Flowline] data you previously exported from a vignette and scales it to fit the mask. 

* **Import Flowlines (Align with View):** Lets you import [!DNL Flowline] data you previously exported from a vignette, keeping it at its original size. 

* **Propagate Resolution To:** Lets you apply the resolution setting for this object to any parent objects or groups. The submenu lists the objects you can specify.

**To Import a UV Map for this Object:** 

1. Select the object whose flowline map you want to replace.
1. Right-click the object in the [ [!DNL Object Explorer]](../../../../r-vat-glossary/c-vat-obj-explorer.md#concept-da56038ea82c40a1a10576f99f2f6836) and choose **[!UICONTROL Properties]**.
1. Click the **[!UICONTROL Map]** tab.
1. Click **[!UICONTROL Action]**.
1. Click **[!UICONTROL Load map image from file]**.
1. Navigate to the [!DNL .RLA] file you want to import as your flowline map. Select the file and click **[!UICONTROL OK]**.
1. Click **[!UICONTROL OK]** in the [!DNL Properties] dialog box.
