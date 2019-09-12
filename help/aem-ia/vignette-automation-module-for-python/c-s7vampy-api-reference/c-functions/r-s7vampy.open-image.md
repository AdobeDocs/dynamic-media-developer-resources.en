---
description: Open an image file.
seo-description: Open an image file.
seo-title: s7vampy.open_image(filename)
title: s7vampy.open_image(filename)
uuid: 949dd932-921f-4fe7-b384-8e63e65c7b75
index: y
internal: n
snippet: y
---

# s7vampy.open_image(filename){#s-vampy-open-image-filename}

Open an image file.

<table id="table_BC918FA22C4F46E6B563EED6D234CB6D"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p><span class="codeph"> filename (str)</span> </p> <p>Name of the image file that is loaded into memory. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"><a href="../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a></span> </p> <p> The image instance. </p> </td> 
  </tr> 
 </tbody> 
</table>

The supported image file formats are: BMP, JPEG, PNG, and TIFF.

Support is limited to RGB and grayscale images. Only RGB images can have an alpha channel. The alpha channel can be extracted and used as a mask using the `s7vampy.image.Image.extract_alpha()` method. RGBA images can also be used to build static overlapping objects using the ` [s7vampy.obj.Group.add_static_overlap_object()](../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-staticoverlapobject.md#reference-7b66780df1fc40cfa436fecdc16037c5)` method.

Grayscale images are used to for masks and illumination maps. Note that all images added to a vignette need to match the size of the vignette view image.

**Opening an image:**

```
>>> from s7vampy import *
>>> img = open_image("TestData/view.png")
>>> img {name='TestData/view.png', has_alpha=False, size=(422, 640)}
```

**Failure while opening an image:**

```
>>> from s7vampy import *
>>> open_image("TestData/does-not-exist.png")
Traceback (most recent call last):
RuntimeError: Open Failed: 'TestData/does-not-exist.png'
```

