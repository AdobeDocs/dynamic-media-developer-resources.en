---
description: When you apply a texture to an object, the texture anchor point matches up with the origin on the object to position the texture on the object's surface.
seo-description: When you apply a texture to an object, the texture anchor point matches up with the origin on the object to position the texture on the object's surface.
seo-title: About the Origin
solution: Experience Manager
title: About the Origin
topic: Scene7 Image Authoring
uuid: cae738b4-8c53-4771-bbe1-0088d02e5225
---

# About the Origin{#about-the-origin}

When you apply a texture to an object, the texture anchor point matches up with the origin on the object to position the texture on the object's surface.

You can visualize the process by imagining that you attach one side of a snap fastener to the texture and the other side to the object. [!DNL Image Authoring] snaps the texture onto the object where the two sides of the fastener meet.

Each object in a vignette has a texture origin point. Most objects use only a standard or center-match origin. [!DNL Flowline] objects can use either a center-match origin or a [continuous origin](../../c-vat-flow-pg/c-vat-abt-flow/c-vat-flow-pg-opt.md#concept-ab8e010be60d46c8841f1b00c3501d16). The continuous origin is useful when applying heavily patterned upholstery. It sets the origin for one object relative to an adjacent object, so the texture flows across the objects and you don't have to align textures manually.

Normally, the origin is located within the masked bounds of the object, but if you flow a texture across adjacent objects, you may cause the origin to move off the object.

You can adjust the origin for any object, as follows:

**For Flat, Planar, and Wall Objects (both 2D and 3D):** Use the [ [!DNL Alignment] tool](../../c-vat-obj-pg/c-vat-obj-pg-tools/c-vat-align-tool.md#concept-2ba104eab0df4b00a52c70bbcd8177a8) on the [!DNL Object] page. Click the point on the object where you want the origin (even if that point is outside the masked area).

[To flow textures seamlessly across adjacent flat, planar, or wall objects](../../c-vat-obj-pg/c-vat-work-obj/t-vat-text-adj-planes.md#task-20755dfecbfb49e3aa5ccc3b97b3f4d8), use the [!DNL Match Origin] command on the [!DNL Object] page.

**For Flowline Objects:** Use the [ [!DNL Flowline Texture] tool](../../c-vat-flow-pg/c-vat-test-flow-work/t-vat-origin-flow-obj.md#task-ad68986712984d8098243e0d0373380b) on the [!DNL Flowline] page to position the origin. [To flow the texture seamlessly across flowline objects](../../c-vat-flow-pg/c-vat-test-flow-work/t-vat-match-text.md#task-568d59da3f7e48838669b17fe96fbed0), use the continuous origin and the [!DNL Match Origin] command on the [!DNL Flowline] page.

**For Sketch Objects:** Use the [!DNL Texture] tool to position the origin. [To flow the texture seamlessly across flowline objects](../../c-vat-work-sketch-pg/r-vat-create-sketch-feat/t-vat-create-feat.md#task-c4fd7e414a9445a49b4c2a3cf7425481)with sketch features, use an [!DNL Object Connector] feature.

You don't have to set the origin for Cabinet, Door, or Appliance objects. You cannot set an origin for Non-Texturable objects. 
