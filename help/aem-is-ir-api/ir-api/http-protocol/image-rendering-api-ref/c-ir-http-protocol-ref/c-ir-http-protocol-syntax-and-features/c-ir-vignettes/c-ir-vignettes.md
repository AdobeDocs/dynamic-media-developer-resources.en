---
description: Vignettes are images authored with Dynamic Media Image Authoring for use with Image Rendering.
solution: Experience Manager
title: Vignettes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
---
# Vignettes{#vignettes}

Vignettes are images authored with Dynamic Media Image Authoring for use with Image Rendering.

IR supports two basic types of vignettes, *2D* and *3D*. Room scenes typically are 3D vignettes which can render reflections, while most other scenes, such as apparel or upholstery, are normally 2D vignettes which do not have reflection rendering capability.

Vignettes contain a *view* and a hierarchy of *objects*.

The view is the container for the main image, shared illumination maps, shared reflection maps, and other data associated with the entire image.

The object hierarchy consists of *object groups*, *standard objects* and *overlap objects*.

Each standard object controls an area of the view image, defined with a gray-scale *mask*. The masks of standard objects never overlap. Standard objects cannot be hidden directly, but they may be covered partially or entirely by overlap objects. Most or all objects in a typical vignette are standard objects.

Overlap objects layer on top of the view image and each other. The order of overlap is defined by a z-value assigned to the object. Overlap objects are useful when parts of a scene need to be shown or hidden dynamically.

Several types of objects are supported (both standard and overlap), with each having its own distinct purpose:

* **Planar objects** (in 3D vignettes) and **flat objects** (in 2D vignettes) accept repeatable texture materials. They are typically used for floors, countertops, and other flat surfaces that only require perspective mapping. 

* **Flowline objects** map smoothly shaped curved surfaces such as upholstery and are occasionally used for apparel objects as well. They can be used in both 2D and 3D vignettes, and, if fully authored, will participate in reflection rendering. 
* **Non-texturable objects** only allow color change-outs. They are permitted in both 2D and 3D vignettes. They are either inherently non-texturable, or they can be a planar or flowline object with a special 'No Texture' flag set. This is useful in 3D vignettes to allow objects to participate in reflection rendering, even though the object will accept only solid color materials. 
* **Sketch objects** are best used for fabric objects with folds and wrinkles, such as apparel items. Like flowline objects, they can be used in 2D and 3D vignettes, although application in 3D vignettes is limited. 
* **Wall objects** are similar to planar objects and are only supported in 3D vignettes. They have special layout information that allows application of two different wall finishes (upper and lower) and up to three wall border materials. When properly authored, materials applied to walls will flow accurately and seamlessly between adjacent walls, for realistic wallpaper/wall border applications. Wall objects do not support texture rotation. 
* **Cabinet objects** are permitted in 3D vignettes only. They are used to author kitchen and bath cabinets with complex layout requirements. Cabinet objects accept repeatable textures as well as specially authored *cabinet style files* containing resizable cabinet panel images.

In addition to the basic object types, two special kinds of overlap objects are supported:

* **Static overlap objects** are objects which do not accept materials. They are permitted in both 2D and 3D vignettes. They are useful for removable accessories in a room scene, for drop shadows behind renderable overlap objects, and similar applications. 
* **Window covering frame objects** provide placement information for applying window coverings style files, which are authored independently of the vignette and can be shared amongst vignettes.

Objects are collected into *object groups*, similar to a file system. Grouping is normally based on the structure of the physical objects they represent (e.g a 'All Cabinets' group might contain 'Base Cabinets' and 'Wall Cabinets'). Any number of group levels are permitted. Grouping supports the application of materials to multiple like objects. 

* [Scene coordinates](c-ir-scene-coordinates.md)
* [Material resolution](c-ir-material-resolution.md)
