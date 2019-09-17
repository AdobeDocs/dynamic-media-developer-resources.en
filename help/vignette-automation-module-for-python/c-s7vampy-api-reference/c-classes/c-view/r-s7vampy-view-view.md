---
description: Each master vignette has one view associated with it. The view provides the view image and illumination maps associated with the vignette.
seo-description: Each master vignette has one view associated with it. The view provides the view image and illumination maps associated with the vignette.
seo-title: class s7vampy.view.View(view)
title: class s7vampy.view.View(view)
uuid: 7d7ba5d2-9d7c-47bb-a2e7-754b6daeea23
---

# class s7vampy.view.View(view){#class-s-vampy-view-view-view}

Each master vignette has one view associated with it. The view provides the view image and illumination maps associated with the vignette.

The vignette view either already exists when a vignette is opened, or it is automatically created when a vignette is created by the ` [s7vampy.create_vignette()](../../../c-s7vampy-api-reference/c-functions/r-s7vampy-create-vignette.md#reference-86313ac79bc14fdb9e68e1138c8261e0)` function using the provided view image.

Note that a view must have at least one illumination map associated with it. If that's not the case, the ` [s7vampy.vignette.Vignette.save()](../../../c-s7vampy-api-reference/c-classes/c-vignette/r-class-s7vampy-vignette-vignette.md#reference-b63a48cb2bd04a1d98930e059a0f3678)` method raises an exception.

`alternative_shader [bool]`

Alternative shader.

The alternative shader is turned on by default. It is recommended to leave the alternative shader on.

`default_print_resolution [float]`

Default print resolution.

`default_texture_resolution [float]`

Default texture resolution.

The default texture resolution setting is used when new surface objects are created.

`gloss_effects [bool]`

Gloss effects. Extrapolate or interpolate illumination based on gloss.

Gloss effects is turned on by default when a new vignette is created.

`illum [s7vampy.illum.IlluminationMaps]`

Global illumination maps ( ` [s7vampy.illum.IlluminationMaps](../../../c-s7vampy-api-reference/c-classes/c-illumination-maps/r-s7vampy-illum-illuminationmaps.md#reference-c8173b275d4247ed854b6baf5781ab2f)`).

Use this property to define one or more global illumination maps for the view.

`image [s7vampy.image.Image, read-only]`

Vignette view image ( ` [s7vampy.image.Image](../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94)`).

`name [str]`

Name of the view.

`size [tuple, read-only]`

Vignette view image size in pixels (width, height). 
