---
description: Creates a new vignette with a view defined by the given view image.
seo-description: Creates a new vignette with a view defined by the given view image.
seo-title: s7vampy.create_vignette(image)
title: s7vampy.create_vignette(image)
uuid: 1a70f98b-6765-41f1-a7d8-0ce8eb62c89a
---

# s7vampy.create_vignette(image){#s-vampy-create-vignette-image}

Creates a new vignette with a view defined by the given view image.

<table id="table_C77F09B3B24D481999B512606363282E"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p><span class="codeph">image (<a href="../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a>)</span> </p> <p>View image associated with the initial vignette view. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"><a href="../../c-s7vampy-api-reference/c-classes/c-vignette/r-class-s7vampy-vignette-vignette.md#reference-b63a48cb2bd04a1d98930e059a0f3678" format="dita" scope="local"> s7vampy.vignette.Vignette</a> </span> </p> <p> Vignette instance </p> </td> 
  </tr> 
 </tbody> 
</table>

The vignette contains a background object that masks the entire vignette view.

A vignette needs at least one illumination map, or the vignette cannot be saved.

**Create a minimal vignette:**

```
>>> from s7vampy import *
>>> v = create_vignette(open_image("view.png"))
>>> v.view.illum[0] = open_image("illum.png"))
>>> v.save("minimal.vnt")
```

**Create a vignette with one group and one object:**

```
>>> from s7vampy import *
>>> v = create_vignette(open_image("view.png"))
>>> v.view.illum[0] = open_image("illum.png"))
>>> group = v.objects.add_group("group")
>>> group.add_nontexturable_object("object", open_image("object-mask.png"))
>>> v.save("nontexturable.vnt")
```

