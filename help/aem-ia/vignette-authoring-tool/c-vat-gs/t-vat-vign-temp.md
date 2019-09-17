---
description: If you use a standardized approach for naming groups, sub-groups, and objects in your vignettes, you can create a vignette that contains these names.
seo-description: If you use a standardized approach for naming groups, sub-groups, and objects in your vignettes, you can create a vignette that contains these names.
seo-title: Using a Vignette as a Template
solution: Experience Manager
title: Using a Vignette as a Template
topic: Scene7 Image Authoring
uuid: 5d9adbe2-92e1-4eff-8d44-ba94df03da7b
---

# Using a Vignette as a Template{#using-a-vignette-as-a-template}

If you use a standardized approach for naming groups, sub-groups, and objects in your vignettes, you can create a vignette that contains these names.

You can then make that vignette a template. When you attach the template to a vignette, you can use its definitions for groups, sub-groups, and objects on the [!DNL Object] page, ensuring consistency and correct spelling.

**To Create a Template:** 

1. [Create a new vignette](../c-vat-gs/t-vat-create-vign.md#task-a51b7fb4cce14ea88279116b24cc98b4).

   Use a small image for the vignette, since the image itself won't matter when you attach the template to a real vignette. However, every vignette must have an image. 

1. On the [!DNL Object] page, create the set of [groups](../c-vat-obj-pg/c-vat-create-grps-obj/t-vat-create-grps.md#task-1c2ae5cfaf3a4c51b153eea44dc3d099), [sub-groups](../c-vat-obj-pg/c-vat-create-grps-obj/c-vat-abt-sub-grps.md#concept-bb725e89c8104e6ca2501ffadde6bfb2), and [2D](../c-vat-obj-pg/c-vat-create-grps-obj/t-vat-create-2d-obj.md#task-b0c168d6f127408c882e8f1de36c8bc7) or [3D](../c-vat-obj-pg/c-vat-create-grps-obj/t-vat-create-3d-obj.md#task-adac1e1e26024993aa97ed6c7e87c084) objects you want to save with the template.

   Save only objects of the same type-2D or 3D. If you are creating a template for a particular type of image (for example, living-room shots), create only the groups, sub-groups, and objects you will use in that type of vignette. It is important to differentiate between 2D and 3D objects because there are problems when trying to render two objects of different types.

   The template sets the default object-creation mode to 2D or 3D, depending on the setting in the vignette you use to create the template. 

1. Without doing any further authoring work, save and close the vignette.
1. Use Windows Explorer to copy the vignette you just saved into the [!DNL \Templates] folder under the [!DNL Image Authoring] folder.

   By default, [!DNL Image Authoring] is installed in [!DNL c:\Program Files\Scene7\Image Authoring].

   The template now appears in the pull-down list on the [ [!DNL Vignette Properties]](../c-vat-gs/t-vat-create-vign.md#task-a51b7fb4cce14ea88279116b24cc98b4) dialog box. You can attach this template to a [new](../c-vat-gs/t-vat-create-vign.md#task-a51b7fb4cce14ea88279116b24cc98b4) or an [existing](../c-vat-gs/t-vat-att-temp-vign.md#task-85731ad3e7764927977e0d0b2a11390e) vignette. 

