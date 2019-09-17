---
description: A non-texturable object is an object that can only be colorized. During rendering the masked area is colorized using the illumination map.
seo-description: A non-texturable object is an object that can only be colorized. During rendering the masked area is colorized using the illumination map.
seo-title: class s7vampy.obj.NonTexturableObject(parent, obj)
title: class s7vampy.obj.NonTexturableObject(parent, obj)
uuid: ea9dc9e4-843c-42fb-954a-28a18004cd27
---

# class s7vampy.obj.NonTexturableObject(parent, obj){#class-s-vampy-obj-nontexturableobject-parent-obj}

A non-texturable object is an object that can only be colorized. During rendering the masked area is colorized using the illumination map.

Regular non-texturable objects use the global illumination map that is defined in the vignette view. Overlapping non-texturable objects use the local illumination map that is defined in the object itself. (See the `illum` property.)

See also: ` [Object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-object.md#reference-6b1486208ad24966b84942e03e5ae9ad)` - Base class

`illum [s7vampy.illum.IlluminationMaps]`

Local illumination maps ( ` [s7vampy.illum.IlluminationMaps](../../../c-s7vampy-api-reference/c-classes/c-illumination-maps/r-s7vampy-illum-illuminationmaps.md#reference-c8173b275d4247ed854b6baf5781ab2f)`).

Local illumination maps are only available for overlap objects.

`mask [s7vampy.image.Image, read-only]`

Mask image ( ` [s7vampy.image.Image](../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94)`).

The mask image is the same size as the vignette view image.

`rect [tuple, read-only]`

Object bounding box in the view image (x, y, width, height).

`z_order [int]`

Z-order (int, range 0 - 1000).

The `z_order` property is only available for overlap objects.

New overlap objects have their `z_order` property automatically initialized to be higher than existing overlap objects in the vignette.

>[!NOTE]
>
>No two overlap objects within a single vignette are allowed to use the same z-order value.

