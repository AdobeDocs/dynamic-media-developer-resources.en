---
description: Opens an existing vignette and allows a script to inspect or update vignettes.
seo-description: Opens an existing vignette and allows a script to inspect or update vignettes.
seo-title: s7vampy.open_vignette(filename, writable=False)
title: s7vampy.open_vignette(filename, writable=False)
uuid: 449d2d2a-e89c-4f74-a71e-9d01e4d313b9
index: y
internal: n
snippet: y
---

# s7vampy.open_vignette(filename, writable=False){#s-vampy-open-vignette-filename-writable-false}

Opens an existing vignette and allows a script to inspect or update vignettes.

<table id="table_1E19D1F61F9A4B74823683DE9FDF1862"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_BD0E59A06A734232A9AA2E3884D01B1C"> 
      <li id="li_392D7E33EBAB426886F94B4555ADFE99"><span class="codeph"> filename(str)</span> <p>Name of the vignette file that is loaded into memory. </p> </li> 
      <li id="li_2E193B585F864D948D1547F2C0C2DE5A"><span class="codeph"> writable(bool)</span> <p>True, if the vignette is saved back to disk. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"><a href="../../c-s7vampy-api-reference/c-classes/c-vignette/r-class-s7vampy-vignette-vignette.md#reference-b63a48cb2bd04a1d98930e059a0f3678" format="dita" scope="local"> s7vampy.vignette.Vignette</a></span> </p> <p>Vignette instance </p> </td> 
  </tr> 
 </tbody> 
</table>

**Open an existing vignette, and show the objects: **

```
>>> from s7vampy import *
>>> v = open_vignette("my-vignette.vnt")
>>> for o in v.objects:
... print o.path
group1
group1/object1
group2
group2/object1
```

