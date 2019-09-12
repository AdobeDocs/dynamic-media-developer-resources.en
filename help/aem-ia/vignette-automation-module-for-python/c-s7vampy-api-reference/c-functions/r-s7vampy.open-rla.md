---
description: Open a RLA file from disk.
seo-description: Open a RLA file from disk.
seo-title: s7vampy.open_rla(filename)
title: s7vampy.open_rla(filename)
uuid: 386c839e-61c1-49a3-b3c6-23e38bcebcdf
index: y
internal: n
snippet: y
---

# s7vampy.open_rla(filename){#s-vampy-open-rla-filename}

Open a RLA file from disk.

<table id="table_5C252731C0C6488CB09C751BCD2DFD88"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p><span class="codeph"> filename (str)</span> </p> <p> Name of the RLA file that is loaded into memory. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"> RLA</span> </p> <p>The RLA instance </p> </td> 
  </tr> 
 </tbody> 
</table>

RLA (Run-Length Encoded, Version A) files can include arbitrary image channels. In the context of the Vignette Automation Module, an RLA file is used to load in UV coordinates. These UV coordinates are then used to render and flow textures and decals on objects.

**Associate UV coordinate from an RLA image with an object:**

```
>>> from s7vampy import *
>>> # Create a new vignette using view.png as the view image
>>> v = create_vignette(open_image("view.png"))
>>> # Use illum.png as illumination map A
>>> v.illum[0] = open_image("illum.png")
>>> # Create a group named "group"
>>> g = v.objects.add_group("group")
>>> # Create a surface object located at "group/surface"
>>> obj = g.add_surface_object("surface", open_image("surface-mask.png"))
>>> # Load UV coordinates from surface-uv.rla
>>> obj.uv_image = open_rla("surface-uv.rla")
```

