---
description: Decals are positioned according to the decal anchor point.
seo-description: Decals are positioned according to the decal anchor point.
seo-title: Configure the Decal Anchor Point
title: Configure the Decal Anchor Point
uuid: ec7ea5e3-9d3a-494c-b9bb-1497c110322c
---

# Configure the Decal Anchor Point{#configure-the-decal-anchor-point}

Decals are positioned according to the decal anchor point.

The decal anchor point is initially the same as the default origin point (origin point 0).

Decal anchor points are provided in view coordinates (pixels).

>[!IMPORTANT]
>
>The decal anchor point is stored in the vignette relative to the default origin point. This means that when the default origin point moves, it also moves the decal anchor point.

Example:

```
>>> from s7vampy import *
>>> v = create_vignette(open_image("view-image.png"))
>>> v.view.illum[0] = open_image("view-illum.png")
>>> group = v.objects.add_group("group")
>>> obj = group.add_surface_object("obj", open_image("obj-mask.png"))
>>> obj.uv_image = open_rla("obj-uv.rla")
>>> obj.resolution = obj.optimal_resolution
>>> obj.origins[0] = (50, 50)
>>> obj.origins.decal = (150, 50)
>>> v.save("new-vignette.vnt")
```

This script builds on top of the previous script and configures the decal anchor point to be at (150, 50). Again, this only works if (150, 50) is on the object mask. 
