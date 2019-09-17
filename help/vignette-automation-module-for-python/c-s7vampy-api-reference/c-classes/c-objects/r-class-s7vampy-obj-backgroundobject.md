---
description: A vignette contains one background object. The background object is not renderable. The background object masks the areas of the vignette view image that are not masked by the object masks.
seo-description: A vignette contains one background object. The background object is not renderable. The background object masks the areas of the vignette view image that are not masked by the object masks.
seo-title: class s7vampy.obj.BackgroundObject(parent, obj)
title: class s7vampy.obj.BackgroundObject(parent, obj)
uuid: 45428163-0bbc-47d3-907c-dd72aaea0284
---

# class s7vampy.obj.BackgroundObject(parent, obj){#class-s-vampy-obj-backgroundobject-parent-obj}

A vignette contains one background object. The background object is not renderable. The background object masks the areas of the vignette view image that are not masked by the object masks.

See also [Object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-object.md#reference-6b1486208ad24966b84942e03e5ae9ad) - Base class

`mask [s7vampy.image.Image, read-only]`

Mask image ( ` [s7vampy.image.Image](../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94)`).

The mask image is the same size as the vignette view image.

`rect [tuple, read-only]`

Object bounding box in the view image (x, y, width, height). 
