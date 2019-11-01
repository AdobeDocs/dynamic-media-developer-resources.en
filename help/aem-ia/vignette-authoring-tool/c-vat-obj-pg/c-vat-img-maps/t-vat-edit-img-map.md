---
description: You may want to edit image map areas that are divided into many small areas, to redefine them as a single area.
seo-description: You may want to edit image map areas that are divided into many small areas, to redefine them as a single area.
seo-title: Editing an Image Map
solution: Experience Manager
title: Editing an Image Map
topic: Scene7 Image Authoring
uuid: 70116343-8521-4ea9-b131-5573df7383d7
---

# Editing an Image Map{#editing-an-image-map}

You may want to edit image map areas that are divided into many small areas, to redefine them as a single area.

This helps to ensure that the user selects the intended object when he clicks. Changes to the image map do not affect changes to the object masks.

Do not completely enclose any area on the image map if that area contains another object. Doing so prevents the interior object from being rendered. For example, if you draw a complete rectangle around a tabletop in your image map, any objects that are fully within that rectangle won't render.

**To Edit an Image Map:** 

1. [Generate the image map](../../c-vat-obj-pg/c-vat-img-maps/t-vat-create-img-map.md#task-a6fa69cb34ce4244ab31940c4de08f59) with the [!DNL Image Map] tool ![](assets/image_map.png).
1. To see the image map for an object group, make sure the [!DNL Image Map] tool is still selected and select the group in the [ [!DNL Object Explorer.]](../../r-vat-glossary/c-vat-obj-explorer.md#concept-da56038ea82c40a1a10576f99f2f6836)

   Make sure you select a group and not an object. 

1. Click any polygon in the map for this group to edit it.

   The polygon turns yellow when it is selected. 

1. Once the polygon is selected, you can do any of the following:

    * Drag the vertexes on the polygon to reshape it. To move a vertex one pixel at a time, use the arrow keys. This process is similar to defining a mask . You may want to make the polygon slightly larger than the masked area, so the user does not click outside it by mistake. 
    * Click anywhere on the yellow outline to add a vertex. 
    * To delete a polygon in the group, right-click the selected polygon and choose **[!UICONTROL Delete Selected Polygon]**. If the group contains many small polygons, you may want to delete all but one, then stretch that one to cover the entire group area. 
    * Right-click a vertex on the polygon and choose **[!UICONTROL Delete Vertex]** or **[!UICONTROL Delete Vertex in Opposite Direction]**. The vertex to the left or right of the one you clicked is deleted.

>[!MORELIKETHIS]
>
>* [Creating an Image Map](../../c-vat-obj-pg/c-vat-img-maps/t-vat-create-img-map.md#task-a6fa69cb34ce4244ab31940c4de08f59)
>* [Exporting an Image Map](../../c-vat-obj-pg/c-vat-img-maps/t-vat-exp-img-map.md#task-15fc6689062e49b098a698d6621a793b)
