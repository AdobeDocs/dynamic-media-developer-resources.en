---
description: Use these steps to associate data with surface objects.
seo-description: Use these steps to associate data with surface objects.
seo-title: Surface Objects
title: Surface Objects
uuid: 69b1e325-8f77-42b2-a281-def7886cc73b
index: y
internal: n
snippet: y
---

# Surface Objects{#surface-objects}

Use these steps to associate data with surface objects.

1. Associate a UV image or RLA file with the objects.
1. Set the size and resolution of the object (optional).
>
>>[!NOTE]
>>
>>Image Authoring does not have an object named Surface. A Surface Object appears as a Flowline Object in Image Authoring. 
>
>The resolution of a newly added surface objects is set to the value of `default_texture_resolution` configured for the view. This resolution is also used to calculate the initial size of the object in inches. 
>
>A script could use the `optimal_resolution` property, available only for surface objects, to set the object resolution to the optimal resolution as calculated from the UV image and the current object size. 
>
>If both the size and resolution of a surface object need to be changed, it is recommended to use the `set_size_resolution` method. The method validates the passed-in size and resolution together as a single entity. Changing the size by itself causes a validation with the existing resolution. Changing the resolution by itself causes a validation with the existing size. This may raise an exception if the changed size causes the existing resolution to become excessive, or if the changed resolution is excessive when used with the existing size. 
>
>Example: 
>
>```>
>>>> from s7vampy import *
>>>> v = create_vignette(open_image("view-image.png"))
>>>> v.view.illum[0] = open_image("view-illum.png")
>>>> group = v.objects.add_group("group")
>>>> obj = group.add_surface_object("obj", open_image("obj-mask.png"))
>>>> obj.uv_image = open_rla("obj-uv.rla")
>>>> obj.resolution = obj.optimal_resolution
>>>> v.save("new-vignette.vnt")
>```>
>This script adds a new surface object that gets its texture coordinates from the [!DNL obj-uv.rla] file and sets the object resolution to the optimal resolution as calculated from the UV image. 

