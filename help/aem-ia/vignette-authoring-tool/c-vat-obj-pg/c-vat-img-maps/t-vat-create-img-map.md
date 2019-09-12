---
description: Image maps are used only on websites that support dynamic rendering.
seo-description: Image maps are used only on websites that support dynamic rendering.
seo-title: Creating an Image Map
solution: Experience Manager
title: Creating an Image Map
topic: Scene7 Image Authoring
uuid: 69111edb-a619-4ee8-b3e4-ea1be1c9903a
index: y
internal: n
snippet: y
---

# Creating an Image Map{#creating-an-image-map}

Image maps are used only on websites that support dynamic rendering.

The areas on the image map become the clickable areas on the website.

If you plan to implement image maps, you can [generate one automatically](../../c-vat-obj-pg/c-vat-obj-pg-tools/c-vat-img-map-tool.md#concept-302430319bce46ebb4e1cfbe495bcb75) with the [!DNL Image Map] tool, then [edit the resulting map](../../c-vat-obj-pg/c-vat-img-maps/t-vat-edit-img-map.md#task-c36b75f043b3402da9caf6062f8231ba). The automatic image map creates clickable areas that match the object masks in your image.

Do not completely enclose any area on the image map if that area contains another object. Doing so prevents the interior object from being rendered. For example, if you draw a complete rectangle around a tabletop in your image map, any objects that are fully within that rectangle won't render.

** To Create an Image Map:** 

1. Create your [groups](../../c-vat-obj-pg/c-vat-create-grps-obj/t-vat-create-grps.md#task-1c2ae5cfaf3a4c51b153eea44dc3d099), sub-groups, and [objects](../../c-vat-obj-pg/c-vat-create-grps-obj/t-vat-create-2d-obj.md#task-b0c168d6f127408c882e8f1de36c8bc7).
1. [Add masks](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-add-mask.md#task-f8d4ae100d834ace9f90f7f260bf15aa) for the objects.
1. When all the masks are finished, click the **[!UICONTROL Object Page]** button ![](assets/object_page.png).
1. On the [!DNL Object] page, click the **[!UICONTROL Image Map]** tool ![](assets/image_map.png).
1. Right-click in the image and choose **[!UICONTROL Generate Image Map]**.
1. To see the image map for an object group, select the group in the [ [!DNL Object Explorer]](../../r-vat-glossary/c-vat-obj-explorer.md#concept-da56038ea82c40a1a10576f99f2f6836).

   You must select a *group* and not an *object*.

>[!MORE_LIKE_THIS]
>
>* [Editing an Image Map](../../c-vat-obj-pg/c-vat-img-maps/t-vat-edit-img-map.md#task-c36b75f043b3402da9caf6062f8231ba)
>* [Exporting an Image Map](../../c-vat-obj-pg/c-vat-img-maps/t-vat-exp-img-map.md#task-15fc6689062e49b098a698d6621a793b)
