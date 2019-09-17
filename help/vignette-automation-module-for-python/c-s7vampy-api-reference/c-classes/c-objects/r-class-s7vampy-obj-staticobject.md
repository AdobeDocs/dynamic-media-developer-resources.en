---
description: A static object only masks out an area from the view image, so that it is not included in the background mask. A static object is not renderable.
seo-description: A static object only masks out an area from the view image, so that it is not included in the background mask. A static object is not renderable.
seo-title: class s7vampy.obj.StaticObject(parent, obj)
title: class s7vampy.obj.StaticObject(parent, obj)
uuid: a906f8ca-44c8-4e15-8d7c-38bf7a559ca8
---

# class s7vampy.obj.StaticObject(parent, obj){#class-s-vampy-obj-staticobject-parent-obj}

A static object only masks out an area from the view image, so that it is not included in the background mask. A static object is not renderable.

See also: ` [Object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-object.md#reference-6b1486208ad24966b84942e03e5ae9ad)` - Base class

`mask [read-only, s7vampy.image.Image]`

Mask image ( ` [s7vampy.image.Image](../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94)`).

The mask image is the same size as the vignette view image.

`rect [tuple, read-only]`

Object bounding box in the view image (x, y, width, height). 
