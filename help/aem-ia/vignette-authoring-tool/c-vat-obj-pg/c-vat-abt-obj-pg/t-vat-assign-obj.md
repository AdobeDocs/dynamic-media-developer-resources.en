---
description: After you create and import the geometry skeleton, you must assign a specific 3D plane to each planar object and each 3D Flowline or Sketch object in your vignette.
seo-description: After you create and import the geometry skeleton, you must assign a specific 3D plane to each planar object and each 3D Flowline or Sketch object in your vignette.
seo-title: Assigning Objects to Planes
solution: Experience Manager
title: Assigning Objects to Planes
topic: Scene7 Image Authoring
uuid: b082160c-f962-4643-b561-65b166729b20
---

# Assigning Objects to Planes{#assigning-objects-to-planes}

After you create and import the geometry skeleton, you must assign a specific 3D plane to each planar object and each 3D Flowline or Sketch object in your vignette.

For example, you can join a wall object to a vertical geometric plane. Once you assign an object to a plane, it moves and sizes to that plane.

Assign [ [!DNL 3D Flowline] or [!DNL Sketch] objects](../../c-vat-obj-pg/c-vat-create-grps-obj/t-vat-create-3d-obj.md#task-adac1e1e26024993aa97ed6c7e87c084) to the planes that reflect them. Only that plane can see the assigned objects. Other planes ignore them.

**To Assign an Object to a Plane:** 

1. [Mask](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-add-mask.md#task-f8d4ae100d834ace9f90f7f260bf15aa) the objects you want to assign to planes.
1. Click the **[!UICONTROL 3D Import]** tool ![](assets/import.png).

   You see the geometry skeleton. The skeleton represents the boundaries of the planes you defined on the [!DNL 3D Modeling] page. 

1. Click within the boundary of a geometric plane to select it.
1. Alt-click the object in the image to assign to the selected plane.
1. Right-click the image and choose **[!UICONTROL Set Plane]**.

   You can assign several planar objects to the same plane. Alt-click another object and choose **[!UICONTROL Set Plane]** again to assign the new object to the same plane. 

If you change the camera or scale on the [!DNL 3D Modeling] page, you must reassign all objects to planes. If you change a plane on the [!DNL 3D Modeling] page, you must reassign its objects. 
