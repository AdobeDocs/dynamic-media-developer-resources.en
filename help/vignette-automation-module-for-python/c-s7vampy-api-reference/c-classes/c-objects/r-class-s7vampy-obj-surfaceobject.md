---
description: A surface object is an object that contains a mask and an image with encoded UV coordinates. The mask, the UV image, and the illumination map are all used to render a texture or decal on a surface object. Surface objects become flowline obects in Image Authoring.
seo-description: A surface object is an object that contains a mask and an image with encoded UV coordinates. The mask, the UV image, and the illumination map are all used to render a texture or decal on a surface object. Surface objects become flowline obects in Image Authoring.
seo-title: class s7vampy.obj.SurfaceObject(parent, obj)
title: class s7vampy.obj.SurfaceObject(parent, obj)
uuid: aee718e5-8d5f-484d-9743-2cd011339c87
---

# class s7vampy.obj.SurfaceObject(parent, obj){#class-s-vampy-obj-surfaceobject-parent-obj}

A surface object is an object that contains a mask and an image with encoded UV coordinates. The mask, the UV image, and the illumination map are all used to render a texture or decal on a surface object. Surface objects become flowline obects in Image Authoring.

Regular surface objects use the global illumination map that is defined in the vignette view. Overlapping surface objects use the local illumination map that is defined in the object itself. (See the `illum` property.)

When a surface object is created initially, the UV image is automatically generated to fit the object mask.

See also: ` [Object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-object.md#reference-6b1486208ad24966b84942e03e5ae9ad)` - Base class

`illum [s7vampy.illum.IlluminationMaps]`

Local illumination maps ( ` [s7vampy.illum.IlluminationMaps](../../../c-s7vampy-api-reference/c-classes/c-illumination-maps/r-s7vampy-illum-illuminationmaps.md#reference-c8173b275d4247ed854b6baf5781ab2f)`).

Local illumination maps are only available for overlap objects.

`mask [s7vampy.image.Image, read-only]`

Mask image ( ` [s7vampy.image.Image](../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94)`).

The mask image is the same size as the vignette view image.

`optimal_resolution [float, read-only]`

Optimal object resolution in pixels/inch.

The optimal object resolution is calculated according to the object mask and the UV image associated with the object.

`origins [s7vampy.origin.OriginPoints]`

Decal and texture origin points ( ` [s7vampy.origin.OriginPoints](../../../c-s7vampy-api-reference/c-classes/c-origin-points/r-class-s7vampy-origin-originpoints.md#reference-9f69831f5d7b420297318b7d56b08e46)`).

`rect [tuple, read-only]`

Object bounding box in the view image (x, y, width, height).

`resolution [float]`

Object resolution in pixels/inch.

` set_size_resolution ( *`width`*, *`height`*, *`resolution`*)`

<table id="table_6A0EBCE7258C447CB2AA6D162DE18490"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_E87C075F43614EA8879E6D6262278FD6"> 
      <li id="li_9CC7510F6439431F912C49C40EF900EE"><span class="codeph">width(<span class="varname"> float</span>)</span>. <p>Object width in inches (must be greater than 0) </p> </li> 
      <li id="li_4608F15BCE834A4C801CD6A6C7220A6D"><span class="codeph">height(<span class="varname"> float</span>)</span> <p>Object height in inches (must be greater than 0). </p> </li> 
      <li id="li_4B3972A6449844E09A1494443924CC9B"><span class="codeph">resolution(<span class="varname"> float</span>)</span> <p>Object resolution in pixels per inch (0.001 - 500). </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Modify both the object size and object resolution at the same time.

It is recommended to call this method when both the object size and resolution have to be modified. Otherwise, the object size and the object resolution are verified independently. This may cause an exception to be raised when the object size is changed and the current object resolution becomes out of range, or when the new object resolution is out of range based on the current object size.

`size [tuple]`

Object size in inches (float, float).

Changing the size of a surface object also adjusts the location of the origin points in the view. It is recommended to define the size and resolution of a surface object before defining the origin points.

`uv_image`

UV image.

An UV image can be changed using either an ` [s7vampy.image.Image](../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94)` instance or an ` [s7vampy.rla.RLA](../../../c-s7vampy-api-reference/c-classes/c-rla/r-class-s7vampy-rla.md#reference-03a1d066982b4b699ac4ef2433c4cee4)` instance. UV images retrieved from a vignette are always ` [s7vampy.image.Image](../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94)` instances.

The UV image or RLA must be the same size as the view image, or a `RuntimeError` exception is raised.

`z_order [int]`

Z-order (int, range 0 - 1000).

The `z_order` property is only available for overlap objects.

New overlap objects have their `z_order` property automatically initialized to be higher than existing overlap objects in the vignette.

>[!NOTE]
>
>No two overlap objects within a single vignette are allowed to use the same `z-order` value.

