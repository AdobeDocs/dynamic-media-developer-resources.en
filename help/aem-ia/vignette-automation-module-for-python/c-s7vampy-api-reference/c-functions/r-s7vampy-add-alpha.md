---
description: Add an alpha channel to an RGB image.
seo-description: Add an alpha channel to an RGB image.
seo-title: s7vampy.add_alpha(image)
title: s7vampy.add_alpha(image)
uuid: 26fb3ad7-bd35-44a2-999e-15559c6fd65e
index: y
internal: n
snippet: y
---

# s7vampy.add_alpha(image){#s-vampy-add-alpha-image}

Add an alpha channel to an RGB image.

You can use this function to combine an RGB image with an alpha channel to create an RGBA image that can be used to create static overlapping objects.

<table id="table_71A9B9E94D4C412181518BB5937C75BD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Parameter image: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> image</span> </p> <p>Path to RGB image file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameter alpha: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> alpha</span> </p> <p>Alpha channel to add </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Returns: </p> </td> 
   <td> <p><span class="codeph"><a href="../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a></span> </p> <p> RGBA image. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Adding an alpha channel to an image:**

```
 >>> from s7vampy import *
>>> img = open_image("TestData/image.png")
>>> img
{name='TestData/image.png', has_alpha=False, size=(422, 640)}
>>> alpha = open_image("TestData/alpha.png")
>>> alpha
{name='TestData/alpha.png', has_alpha=False, size=(422, 640)}
>>> add_alpha(img, alpha)
{name='add_alpha', has_alpha=True, size=(422, 640)} 
```

