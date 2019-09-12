---
description: List of origin points defined for surface and flat objects.
seo-description: List of origin points defined for surface and flat objects.
seo-title: class s7vampy.origin.OriginPoints(obj)
title: class s7vampy.origin.OriginPoints(obj)
uuid: 57d5704c-0947-41ef-8cdc-0332e32419b6
index: y
internal: n
snippet: y
---

# class s7vampy.origin.OriginPoints(obj){#class-s-vampy-origin-originpoints-obj}

List of origin points defined for surface and flat objects.

Each texturable object can have one decal anchor point and up to six origin points defined. Origin points are in view coordinates (pixels), and can be indexed by number.

If a given origin point has not been defined, the value of origin point 0 (the default center origin) is returned.

If no origin point has been defined, the default origin for surface objects is set at the UV coordinate (0,0), which gets transformed to a view coordinate (pixels). The exact location of this default depends on the UV image associated with the surface object.

The default origin for flat objects is set to the first point of the perspective quadrilateral.

An exception is raised if an origin point does not lie on the object mask. For surface objects, the following indices can be used:

* 0 - Default (center) origin 
* 1 - Continuous origin 
* 2 - Random origin - Not supported in the Vignette Automation Module 
* 3 - User defined 
* 4 - User defined 
* 5 - User defined 
* 6 - User defined

Changing the size of the surface object using ` [s7vampy.obj.SurfaceObject.size](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-surfaceobject.md#reference-cf2b73b972e84cf5b9a0e22ab3d106f4)` also adjusts the location of the origin points in the view.

It is, therefore, recommended to define the size and resolution of a surface object before defining the origin points.

For flat objects the following indices can be used:

* 0 - Default (center) origin 
* 1 - Continuous origin

The direction of the texture flow ( ` [s7vampy.obj.FlatObject.rotate](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-flatobject.md#reference-e6da5ec8f3564cd088891e6c64205552)`) for flat objects is defined at the default origin point (origin point 0). Because of the perspective transform, changing the position of the default origin point adjusts the direction as well. The effective direction of the texture remains the same.

This class also provides convenient properties to access the default and continuous origin directly.

**Access the default (center) anchor point:**

```
>>> surface_object.origins[0] = (50, 50)
>>> surface_object.origins[0]
(50, 50)
>>> surface_object.origins.default
(50, 50)
```

**Access the decal anchor point:**

```
>>> surface_object.origins.decal = (50, 150)
>>> surface_object.origins.decal
(50, 150)
```

`continuous [tuple]`

Continuous origin in view coordinates (pixels) (float, float).

The continuous origin is at index 1.

`decal [tuple]`

Decal anchor point in view coordinates (pixels) (float, float).

Decals are stored relative to the default origin (origin 0). This means that when the default origin moves, the decal anchor point also moves.

`default [tuple]`

Default (center) origin in view coordinates (pixels) (float, float).

The default (center) origin is at index 0. 
