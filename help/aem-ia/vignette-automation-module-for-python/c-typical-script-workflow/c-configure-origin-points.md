---
description: This optional step is only required if the texture applied to a surface or flat object during rendering needs to start at a specific point.
seo-description: This optional step is only required if the texture applied to a surface or flat object during rendering needs to start at a specific point.
seo-title: Configure Origin Points
title: Configure Origin Points
uuid: fd134add-7547-40fe-b9fd-16fbc2bde2ea
index: y
internal: n
snippet: y
---

# Configure Origin Points{#configure-origin-points}

This optional step is only required if the texture applied to a surface or flat object during rendering needs to start at a specific point.

It is possible to configure from zero to six origin points for surface objects and from zero to two origin points for flat objects. The origin points are provided in view coordinates (pixels). If no origin point is set, textures are positioned at a default position.

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
>>> v.save("new-vignette.vnt")
```

This script adds a surface object with the default center origin point defined as (50, 50) in view coordinates (pixels). Note that this only works if the (50, 50) location is on the object mask; otherwise, an exception is raised. 
