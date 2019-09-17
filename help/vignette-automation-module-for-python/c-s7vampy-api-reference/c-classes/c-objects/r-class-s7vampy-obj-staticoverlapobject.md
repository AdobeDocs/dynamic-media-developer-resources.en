---
description: A static overlapping object provides an RGBA (RGB with alpha) image layer on top of the rendered vignette. The image can be shown or hidden using the usual overlap commands.
seo-description: A static overlapping object provides an RGBA (RGB with alpha) image layer on top of the rendered vignette. The image can be shown or hidden using the usual overlap commands.
seo-title: class s7vampy.obj.StaticOverlapObject(parent, obj)
title: class s7vampy.obj.StaticOverlapObject(parent, obj)
uuid: 76d26fae-7f62-47ae-80df-7f915d2e50d2
---

# class s7vampy.obj.StaticOverlapObject(parent, obj){#class-s-vampy-obj-staticoverlapobject-parent-obj}

A static overlapping object provides an RGBA (RGB with alpha) image layer on top of the rendered vignette. The image can be shown or hidden using the usual overlap commands.

See also: ` [Object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-object.md#reference-6b1486208ad24966b84942e03e5ae9ad)` - Base class

`image [s7vampy.image.Image, read-only]`

Static overlapping object image ( ` [s7vampy.image.Image](../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94)`).

The image must be the same size as the view image, or a `RuntimeError` exception is raised.

`rect [tuple, read-only]`

Object bounding box in the view image (x, y, width, height).

`z_order [int]`

Z-order (int, range 0 - 1000).

The `z_order` property is only available for overlap objects.

New overlap objects have their `z_order` property automatically initialized to be higher than existing overlap objects in the vignette.

>[!NOTE]
>
>No two overlap objects within a single vignette are allowed to use the same z-order value.

