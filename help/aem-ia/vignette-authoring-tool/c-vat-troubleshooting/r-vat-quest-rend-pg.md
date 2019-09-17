---
description: null
seo-description: null
seo-title: Questions About the Render Page
solution: Experience Manager
title: Questions About the Render Page
topic: Scene7 Image Authoring
uuid: 6f4bc892-9630-4575-a11d-eac46716e7bd
---

# Questions About the Render Page{#questions-about-the-render-page}

## What is a material? {#what-is-a-material}

A material is a digital image of the texture you apply in a vignette. This material must be a full repeat. For tips on creating a full repeat, see [Creating a Full-Tile Repeat.](../c-vat-troubleshooting/r-vat-full-tile-repeat/r-vat-full-tile-repeat.md#reference-7dc916534a864b2d9a5d21ca31056b54)

## When I apply a material, how do I know what resolution to set? {#when-i-apply-a-material-how-do-i-know-what-resolution-to-set}

In order to render objects in your vignette effectively, the resolution for the objects in the vignette and the resolution of the materials you apply to them must be set properly. Unlike screen resolution or print resolution settings, resolution settings within [!DNL Image Authoring] refer to world space, or life-size.

You must map texture samples to a resolution by [telling [!DNL Image Authoring] how many pixels in the texture sample correspond to an inch in world space](../c-vat-gs/c-vat-abt-res.md#concept-b15c68590bff427599cb0ee380606a0c). You specify this information on the [!DNL Texture Materials Properties] dialog box that displays when you click ![](assets/finger.png) on the [!DNL Render] page.

## I'm applying a texture to an object, but I can't seem to make the texture the size I want. {#i-m-applying-a-texture-to-an-object-but-i-can-t-seem-to-make-the-texture-the-size-i-want}

The size of the texture depends on two settings:

* On the [!DNL Render] page, the [ [!DNL Resolution]](../c-vat-rend-pg/c-vat-work-text/c-vat-text-mat-prop/c-vat-text-mat-prop.md#concept-56e919cfd48748169dc2f011aa95c5fd). 

* On the [ [!DNL Flowline]](../c-vat-flow-pg/c-vat-use-flow-tools/c-vat-text-tool.md#concept-e54c441b9ea644c0a496cc05c2465ea1) and [ [!DNL Sketch]](../c-vat-flow-pg/c-vat-use-flow-tools/c-vat-text-tool.md#concept-e54c441b9ea644c0a496cc05c2465ea1) pages, the [!DNL Overall] size.

## How do I select an object? {#how-do-i-select-an-object}

Click the drop-down box in the top menu and select your group or object or click once in the appropriate image area to select the group and twice to select the object. Once an object has a mask, you can select it using Alt+click.

## How do I save my rendered images? {#how-do-i-save-my-rendered-images}

You can save a vignette in the native [!DNL Scene7] format (VNT). You can export a vignette in any of these formats: BMP, JPEG, PNG, PSD, and TIFF. When you batch-render images, you can export them as PNG, BMP, JPEG, or TIFF.

## To save a vignette in another format: {#to-save-a-vignette-in-another-format}

1. From the [!DNL File] menu, select **[!UICONTROL Export Image]**. 

1. Name your file and choose a format.

## What format should I use when I save my final image? {#what-format-should-i-use-when-i-save-my-final-image}

This is a personal decision. We recommend saving images in TIFF format to maintain the best quality and resolution. You can always convert to other types after saving.

## How do I create a render set? {#how-do-i-create-a-render-set}

When you [batch render and export the results to IPS](../c-vat-rend-pg/c-vat-rend-obj/t-vat-batch-rend-ips.md#task-f89e8d1a7bc54694b14173505641a0df), you create a render set in IPS.

## Do I need to upload the materials I use before I upload my render set? {#do-i-need-to-upload-the-materials-i-use-before-i-upload-my-render-set}

When you upload a render set, [!DNL Image Authoring] creates a separate swatch for each color or texture you use in this batch-render process and adds those items to IPS as separate files. The entire set of images are stored as a render set within IPS. If the materials were obtained from the company within IPS to which you are uploading, [!DNL Image Authoring] won't upload the materials.

If you plan on using the render set upload, avoid using material images in the TGA image format. IPS does not support that image format and the render set upload fails.

## How do I save a layered image? {#how-do-i-save-a-layered-image}

Use the [!DNL Batch Render] option (under [!DNL Saved Materials]) to set the [!DNL Layered File] option in the [!DNL Batch Render Setup] dialog. 
