---
description: When you create a vignette in Image Authoring, you first define the objects, then apply materials (or textures) to the objects.
seo-description: When you create a vignette in Image Authoring, you first define the objects, then apply materials (or textures) to the objects.
seo-title: About Resolution
solution: Experience Manager
title: About Resolution
topic: Scene7 Image Authoring
uuid: a9eb8cd4-888a-489d-9d6c-6cf6d846ec05
index: y
internal: n
snippet: y
---

# About Resolution{#about-resolution}

When you create a vignette in Image Authoring, you first define the objects, then apply materials (or textures) to the objects.

When a user selects the objects on your Web page, he can apply all the materials you've defined for each object.

In order to render objects in your vignette effectively, you must set the resolution for the objects in the vignette and the resolution of the materials you apply to them. Unlike screen resolution or print resolution settings, resolution settings within [!DNL Image Authoring] refer to world space, or life-size.

* When you create a 2D scene, you can [set the resolution for the entire view](../c-vat-obj-pg/c-vat-abt-obj-pg/t-vat-scale-2d-img.md#task-fd3d9be735144994acf9ebe2e45d84ed) by telling [!DNL Image Authoring] how many pixels in the image correspond to an inch in world space. This works for apparel views and simple scenes in which things appear fairly flat. 

* When you create a 3D scene, you can't set the resolution for the entire view because objects in the background have a different pixel-to-inch ratio than objects in the foreground. For those scenes, you [define the scale](../c-vat-3d-mod-pg/c-vat-create-geo/t-vat-def-3d-scale.md#task-7938e8b9590543a78d48b678d2d26ba9) on the [!DNL 3D Modeling] page, based on one edge of a plane in your 3D model. Based on this scale, [!DNL Image Authoring] calculates an optimal texture resolution for rendering, based on your view image size and object sizes. 

* When you create a texture sample, you must [map the sample to a resolution](../c-vat-flow-pg/c-vat-test-flow-work/t-vat-text-size-flow-obj.md#task-3a9936d1b9c84c238b4e120d1d92a6d9) by telling [!DNL Image Authoring] how many pixels in the texture sample correspond to an inch in world space. You specify this information on the [!DNL Texture Material Properties] dialog box that displays when you click the [!DNL Material Properties] tool on the [!DNL Render] page.

When you make changes with the [!DNL Material Properties] tool, you create a new entry in the [!DNL Material History] list for the changed material. To change the material in the [!DNL Saved Materials] list, right-click the material name in that list and choose [!DNL Properties].

There are two ways to determine the texture resolution:

* You can measure the original swatch and measure the image onscreen at full-size to determine the number of pixels in its width and height, then divide the pixels by the real-life size to find the pixels per inch. 
* If you know that the texture was scaled at 300 dpi and you scaled at 4.5, you can divide 300 by 4.5 to get the same information. If you plan to scale many textures, you may want to set your scale factor so you always end up with the same resolution.

