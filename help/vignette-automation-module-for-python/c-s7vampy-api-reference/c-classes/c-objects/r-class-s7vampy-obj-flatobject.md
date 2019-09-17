---
description: A flat object defines a perspective transform of a rectangle into the vignette view image at a given size (provided in inches).
seo-description: A flat object defines a perspective transform of a rectangle into the vignette view image at a given size (provided in inches).
seo-title: class s7vampy.obj.FlatObject(parent, obj)
title: class s7vampy.obj.FlatObject(parent, obj)
uuid: 6cabc8fc-99ca-4102-9a04-c3fd8254b05d
---

# class s7vampy.obj.FlatObject(parent, obj){#class-s-vampy-obj-flatobject-parent-obj}

A flat object defines a perspective transform of a rectangle into the vignette view image at a given size (provided in inches).

The mask, the perspective transform, and the illumination map are all used to render textures and decals into the transformed rectangle.

Regular flat objects use the global illumination map defined in the vignette view. Overlapping flat objects use the local illumination map defined in the object itself. (See the `illum` property.)

See also: ` [Object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-object.md#reference-6b1486208ad24966b84942e03e5ae9ad)` - Base class

`illum [7vampy.illum.IlluminationMaps]`

Local illumination maps ( ` [s7vampy.illum.IlluminationMaps](../../../c-s7vampy-api-reference/c-classes/c-illumination-maps/r-s7vampy-illum-illuminationmaps.md#reference-c8173b275d4247ed854b6baf5781ab2f)`).

Local illumination maps are only available for overlap objects.

`mask [s7vampy.image.Image, read-only]`

Mask image ( ` [s7vampy.image.Image](../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94)`).

The mask image is the same size as the vignette view image.

`origins [s7vampy.origin.OriginPoints]`

Decal and texture origin points ( ` [s7vampy.origin.OriginPoints](../../../c-s7vampy-api-reference/c-classes/c-origin-points/r-class-s7vampy-origin-originpoints.md#reference-9f69831f5d7b420297318b7d56b08e46)`).

`perspective [s7vampy.path.Path, read-only]`

Perspective quadrilateral ( ` [s7vampy.path.Path](../../../c-s7vampy-api-reference/c-classes/c-path/r-class-s7vampy-path-path.md#reference-2e340c8f51db4053877c584873a41bea)`).

The points provided in the path are in view coordinates (pixels).

`rect [tuple, read-only]`

Object bounding box in the view image (x, y, width, height).

`resolution [float, read-only]`

Object resolution in pixels/inch (float).

`rotate [float]`

Angle at which the texture flows in the perspective quadrilateral (range is -360 to 360).

The angle is provided in degrees, and is relative to the default left to right direction. The angle is clockwise, meaning that an angle of 90 degrees flows the texture top to bottom.

The direction of the texture flow is defined at the default origin point (origin point 0). Because of the perspective transform, changing the position of the default origin point adjusts the angle defined by this property. The effective direction of the texture is still the same.

`  set_perspective ( *`path`*, *`width=0`*, *`height=0`*) `

<table id="table_98DC925B1F754107A182229BDA9CEE28"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_15E3A02796284937B0DC992B628F1DB8"> 
      <li id="li_C52293D63A3F478DA76ECC1701757B98">path( <span class="codeph"> <a href="../../../c-s7vampy-api-reference/c-classes/c-path/r-class-s7vampy-path-path.md#reference-2e340c8f51db4053877c584873a41bea" format="dita" scope="local"> s7vampy.path.Path </a> </span>) <p>Perspective path with one contour and four line segments. </p> </li> 
      <li id="li_86C3B2EE49554786971AA4F1D39799F7"> <span class="codeph"> width( <span class="varname"> float </span>) </span> <p>Width of the perspective quadrilateral in inches. </p> </li> 
      <li id="li_CDDF2FD11B864ABFBA3C620136B98E6A"> <span class="codeph"> height( <span class="varname"> float </span>) </span> <p>Height of the perspective quadrilateral in inches. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Together with the defined mask, `set_perspective` uses the provided quadrilateral and size to define a perspective transform.

The provided path must contain one contour with four line segments. Any other path is rejected. The path is transformed into a quadrilateral by extracting the four points in order.

The points provided in the path are expected to be in view coordinates (pixels).

Behavior is undefined if the quadrilateral is not suitable for a perspective transform (for example, if two or more vertices coincide, if three or all vertices are on the same line, or if the quadrilateral is self-intersecting or concave).

It is possible not to specify either width or height, in which case the missing parameter is calculated. For instance, in the example below, the width parameter is automatically calculated:

```
 >>> flat_object.set_perspective(path, height=5.0)
```

An exception is raised if both width and height are 0.

`size [tuple, read-only]`

Object size in inches (float, float).

`z_order [int]`

Z-order (int, range 0 - 1000).

The `z_order` property is only available for overlap objects.

New overlap objects have their `z_order` property automatically initialized to be higher than existing overlap objects in the vignette.

>[!NOTE]
>
>No two overlap objects within a single vignette are allowed to use the same z-order value.

