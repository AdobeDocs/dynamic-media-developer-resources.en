---
description: null
seo-description: null
seo-title: Mask tab for objects
solution: Experience Manager
title: Mask tab for objects
topic: Scene7 Image Authoring
uuid: 7104d617-1b17-4070-b2f7-0ee87558c478
index: y
internal: n
snippet: y
---

# Mask tab for objects{#mask-tab-for-objects}

 **Offset:** The pixel offset of the top left corner of the bounding rectangle of the mask relative to the top left corner of the image. If you [import a mask](../../../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-imp-mask.md#task-48b7eadbdd7a4b23a3b34d14b59ce787), set the offset (usually to 0,0) before loading the mask image.

**Load:** Use this option to import a mask from external applications, such as [!DNL Photoshop]. When you load mask information, you replace the mask for the current object without changing the masks for adjacent objects. Use this option when you import masks that are already synched to each other and do not overlap, or if you plan to move mask information back and forth between [!DNL Image Authoring] and another image editing application. After you import a mask with this option set, [resync](../../../../c-vat-work-mask-pg/c-vat-abt-mask-pg/c-vat-abt-mask-pg.md#concept-1056cf790a8c41a1b1f8d586b2e85c6b) your image on the [!DNL Mask] page.

**Show:** Creates a view of the mask for this object in a separate window. You can save this view at its actual size using the [!DNL Save As] command. This is a read-only view, so you can't edit it.

**Export:** Saves the mask image at the same size as the full image, filling in the area around the mask with black. You can export in [!DNL .PNG] format only. 
