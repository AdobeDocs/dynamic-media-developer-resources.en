---
description: null
seo-description: null
seo-title: Questions About the Object Page
solution: Experience Manager
title: Questions About the Object Page
topic: Scene7 Image Authoring
uuid: c7563792-7801-45a9-9791-1fe4caf53897
---

# Questions About the Object Page{#questions-about-the-object-page}

## What is a hierarchy? {#what-is-a-hierarchy}

A hierarchy lets you organize your vignette into groups and/or sub-groups with objects in each. This organization lets you control how the vignette is rendered.

## What are groups, sub-groups and objects? {#what-are-groups-sub-groups-and-objects}

A group controls or links a set of objects together.

A sub-group is a group within a group.

An object is a part of a group or sub-group. Each object is a surface area in a vignette that can be uniquely changed.

Every vignette is divided into groups containing objects. Complex vignettes require sub-grouping.

Divide a vignette into several objects if:

* The image is typically made out of different fabrics, and/or 
* The pattern flows in different directions on different parts (objects) of the image.

Grouping aids in rendering by applying the same texture to all objects within the group with one click. A vignette's hierarchy shows all the groups, sub-groups, and objects in a window to the right of the image.

## I want to create an object that can change color only (it won't use textures). Do I need to go to the Flowline Page and edit the Flowline Mesh for the object? {#i-want-to-create-an-object-that-can-change-color-only-it-won-t-use-textures-do-i-need-to-go-to-the-flowline-page-and-edit-the-flowline-mesh-for-the-object}

No. This is only necessary if you intend to apply a texture to the object. When you [create an object](../c-vat-obj-pg/c-vat-work-obj/t-vat-copy-obj.md#task-0b0582d7480a4d6991278ecb688c7823) that receives color only, select a Non-Texturable object on the [!DNL Object] page.

## What is the difference between a Non-Texturable object and a Flowline object? {#what-is-the-difference-between-a-non-texturable-object-and-a-flowline-object}

A Non-texturable object can have only solid materials/colors applied to it. Non-Texturable objects render faster and affect the performance of an [!DNL Image Rendering] server less than [!DNL Flowline] objects do.

A [!DNL Flowline] object can have both solid and patterned/multi-colored materials applied to it.

## Can I change an object type without deleting it and starting over? {#can-i-change-an-object-type-without-deleting-it-and-starting-over}

Yes. Right-click the object to change and convert it to the type of object you need. Values not associated with the new object type can be lost. For example, converting an object with a flowline mesh to a Non-texturable object loses the mesh.

## Why can't I see the Illumination Map? {#why-can-t-i-see-the-illumination-map}

You can view the [!DNL Illumination Map] from the [!DNL Illumination] page by selecting [!DNL Illumination] as the [!DNL Image] option in the side menu. The [!DNL Illumination Map] sits behind the [!DNL View] image. Use the [!DNL View] image to do all of the work required to create a vignette.

## How do I delete my Illumination Map? {#how-do-i-delete-my-illumination-map}

This can be done from the [!DNL Object] page.

**To Delete the Illumination Map:**

1. Ctrl-click ![](assets/finger.png). 
1. Select the **[!UICONTROL Illumination]** tab. 
1. Select the map to delete, click the **[!UICONTROL Action]** button, then choose **[!UICONTROL Delete]**.

