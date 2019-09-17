---
description: Create a RGB image with alpha channel.
seo-description: Create a RGB image with alpha channel.
seo-title: s7vampy.create_rgba(image)
title: s7vampy.create_rgba(image)
uuid: fdc93a7b-0f41-4ba6-970d-198bf7c59644
---

# s7vampy.create_rgba(image){#s-vampy-create-rgba-image}

Create a RGB image with alpha channel.

Create a solid color RGBA image of the given width and height.

Color is specified as a red, green, blue, alpha tuple in the range 0-255. If alpha is omitted then it is set to 255 (solid). If green, blue, and alpha are omitted then a solid gray image is created at the specified red value.

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
>>> img = create_rgba_image(200, 300, (255, 0, 0))
>>> img
{name='rgba_image', has_alpha=True, size=(200, 300)}
```

**Creating a 200x300 solid green image:**

```
>>> from s7vampy import *
>>> img = create_rgba_image(200, 300, 0, 255, 0)
>>> img
{name='rgba_image', has_alpha=True, size=(200, 300)}
```

**Creating a 200x300 solid white image:**

```
>>> from s7vampy import *
>>> img = create_rgba_image(200, 300, 255)
>>> img
{name='rgba_image', has_alpha=True, size=(200, 300)}
```

**Creating a 200x300 solid red image at half transparency:**

```
>>> from s7vampy import *
>>> img = create_rgba_image(200, 300, (255, 0, 0, 128))
>>> img
{name='rgba_image', has_alpha=True, size=(200, 300)}
```

