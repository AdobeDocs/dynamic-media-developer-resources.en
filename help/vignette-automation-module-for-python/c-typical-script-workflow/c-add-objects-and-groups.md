---
description: Next, add objects and groups to the vignette.
seo-description: Next, add objects and groups to the vignette.
seo-title: Add Objects and Groups
title: Add Objects and Groups
uuid: e1e14dd8-fe75-446b-9bbd-0b0cc88f9f73
---

# Add Objects and Groups{#add-objects-and-groups}

Next, add objects and groups to the vignette.

To make sure that images display as expected, objects should be added from back to front. This means that objects that are behind other objects should be added first.

This should be done for non-overlapping objects because the mask of the last added object is preserved over the existing object masks. If two non-overlapping objects mask the same area in the view image, the last added object retains its mask while the existing object that is already masking the area is reduced to remove the conflict. This can't be fixed later on by the script.

Add overlapping objects last because they use a z-order. The automation module automatically increases the z-order (the property that indicates which overlap object is in front of another) for each new overlapping object. The z-order property is automatically initialized to indicate that objects added later should be rendered in front of existing objects. The script can change the z-order property.

Example:

```
>>> from s7vampy import *
>>> v = create_vignette(open_image("view-image.png"))
>>> v.view.illum[0] = open_image("view-illum.png")
>>> group = v.objects.add_group("group")
>>> obj = group.add_nontexturable_object("obj", open_image("obj-mask.png"))
>>> v.save("new-vignette.vnt")
```

This script is an extension of the previous script, but now a non-overlapping object named `obj` is added in the group group. The object uses the mask stored in `obj-mask.png`. 
