---
description: This optional step is only required if an overlapping object needs to be rendered with an illumination map that is different from the illumination map associated with the view.
seo-description: This optional step is only required if an overlapping object needs to be rendered with an illumination map that is different from the illumination map associated with the view.
seo-title: Add Local Illumination Maps for Overlapping Objects
title: Add Local Illumination Maps for Overlapping Objects
uuid: 7eb5419b-e420-495a-9e5f-3d430280403d
index: y
internal: n
snippet: y
---

# Add Local Illumination Maps for Overlapping Objects{#add-local-illumination-maps-for-overlapping-objects}

This optional step is only required if an overlapping object needs to be rendered with an illumination map that is different from the illumination map associated with the view.

Example:

```
>>> from s7vampy import *
>>> v = create_vignette(open_image("view-image.png"))
>>> v.view.illum[0] = open_image("view-illum.png")
>>> group = v.objects.add_group("group")
>>> obj = group.add_nontexturable_object("obj", open_image("obj-mask.png"), overlap = True)
>>> obj.illum[0] = open_image("obj-illum.png")
>>> v.save("new-vignette.vnt")
```

This script adds a non-texturable overlapping object. The local illumination map of the object is defined to be `obj-illum.png`. 
