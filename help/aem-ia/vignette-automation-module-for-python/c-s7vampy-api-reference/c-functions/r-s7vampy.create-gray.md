---
description: Create a gray image.
seo-description: Create a gray image.
seo-title: s7vampy.create_gray(image)
title: s7vampy.create_gray(image)
uuid: 3d9fb764-4dcc-49b7-9f53-4d487439246a
index: y
internal: n
snippet: y
---

# s7vampy.create_gray(image){#s-vampy-create-gray-image}

Create a gray image.

Create a solid color gray image of the given width and height.

<table id="table_71A9B9E94D4C412181518BB5937C75BD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Parameter width int: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> int width</span> </p> <p>Width of the image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameter height int: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> int height</span> </p> <p>Height of the image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameter color tuple: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> color tuple</span> </p> <p>Color of the image. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Returns: </p> </td> 
   <td> <p><span class="codeph"><a href="../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a></span> </p> <p>Image instance. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Creating a 200x300 solid mid-gray image:**

```
>>> from s7vampy import *
>>> img = create_gray_image(200, 300, 128)
>>> img
{name='rgb_image', has_alpha=False, size=(200, 300)} 
```

