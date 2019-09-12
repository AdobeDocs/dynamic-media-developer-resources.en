---
description: You can use the technique described below to apply simple, uniform textures, such as heathering to objects in the image.
seo-description: You can use the technique described below to apply simple, uniform textures, such as heathering to objects in the image.
seo-title: Rendering Heathering and Simple Texture Effects
solution: Experience Manager
title: Rendering Heathering and Simple Texture Effects
topic: Scene7 Image Authoring
uuid: 00a58d72-0f36-44fc-8fbb-6993a00dc3c5
index: y
internal: n
snippet: y
---

# Rendering Heathering and Simple Texture Effects{#rendering-heathering-and-simple-texture-effects}

You can use the technique described below to apply simple, uniform textures, such as heathering to objects in the image.

An example of a heathered texture is the fabric typically used for sweatshirts. The technique described here is not suitable if the texture contains discernible patterns.

**To Apply Simple, Smooth Textures:** 

1. Determine the view resolution.

   To apply a texture, [!DNL Image Authoring] needs to know the size of the object you are authoring. If the scene is simple, for example, if it shows an apparel item laid out flat and photographed straight-on, [!DNL Image Authoring] can determine object sizes based on a common resolution for the view image. This view image resolution is determined by measuring or estimating the distance (in inches) between two arbitrary points in the scene (for example, the width of the shirt), and the distance in pixels between the corresponding points in the image and dividing the latter by the former value, to arrive at a resolution in pixels per inch.

   To determine the distance in pixels between the two points in the scene, you can use the [!DNL Photoshop] Measure tool, or a similar graphics editing tool. 

1. [Set the view resolution](../../c-vat-obj-pg/c-vat-abt-obj-pg/t-vat-scale-2d-img.md#task-fd3d9be735144994acf9ebe2e45d84ed) before creating any objects in the scene.
1. Create [a flowline object](../../c-vat-flow-pg/c-vat-create-flow/t-vat-flow-mesh.md#task-d58bc59e2ad6414d906825834ea5356f) and a [matching mask](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-add-mask.md#task-f8d4ae100d834ace9f90f7f260bf15aa) for each item you plan to render with the heathering texture.

   You don't have to separate apparel items into multiple parts. 

1. [Adjust the [!DNL Illumination Map]](../../c-vat-work-illum-pg/c-vat-work-illum-maps/t-vat-illum-map-img-auth.md#task-0342a45d98cd456aa4e7cbff6a46ca47) if necessary.
1. Apply the [texture](../../c-vat-rend-pg/c-vat-work-text/c-vat-text-mat-prop/c-vat-text-mat-prop.md#concept-56e919cfd48748169dc2f011aa95c5fd).
If you need to change the color, desaturate the heathering texture and brightness before you apply the color. [Vary the resolution](../../c-vat-flow-pg/c-vat-test-flow-work/t-vat-text-size-flow-obj.md#task-3a9936d1b9c84c238b4e120d1d92a6d9) of the heathering texture to control the texture effect. 
