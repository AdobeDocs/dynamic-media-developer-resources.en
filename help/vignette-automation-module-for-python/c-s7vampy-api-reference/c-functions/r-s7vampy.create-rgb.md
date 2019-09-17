---
description: Create an RGB image.
seo-description: Create an RGB image.
seo-title: s7vampy.create_rgb(image)
title: s7vampy.create_rgb(image)
uuid: 912594e7-db4a-4e1f-8610-4ebc10ab1e06
---

# s7vampy.create_rgb(image){#s-vampy-create-rgb-image}

Create an RGB image.

Create a solid color RGB image of the given width and height.

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

**Creating a 200x300 solid red image:**

```
>>> from s7vampy import *
>>> img = create_rgb_image(200, 300, (255, 0, 0))
>>> img
{name='rgb_image', has_alpha=False, size=(200, 300)}
```

**Creating a 200x300 solid green image:**

```
>>> from s7vampy import *
>>> img = create_rgb_image(200, 300, 0, 255, 0)
>>> img
{name='rgb_image', has_alpha=False, size=(200, 300)}
```

**Creating a 200x300 solid white image:**

```
>>> from s7vampy import *
>>> img = create_rgb_image(200, 300, 255)
>>> img
{name='rgb_image', has_alpha=False, size=(200, 300)}
```

