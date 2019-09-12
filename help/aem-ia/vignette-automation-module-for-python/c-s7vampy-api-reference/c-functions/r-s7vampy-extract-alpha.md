---
description: null
seo-description: null
seo-title: s7vampy.extract_alpha(image)
title: s7vampy.extract_alpha(image)
uuid: 06cc6789-015c-4900-8179-8cc1b49c40f6
index: y
internal: n
snippet: y
---

# s7vampy.extract_alpha(image){#s-vampy-extract-alpha-image}

<table id="table_71A9B9E94D4C412181518BB5937C75BD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Parameter: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> image</span> </p> <p>Path to image file. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Returns: </p> </td> 
   <td> <p><span class="codeph"><a href="../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a></span> </p> <p> Grayscale image containing the alpha channel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Extract the alpha channel from the provided image. Returns a grayscale image.

If the provided image does not have an alpha channel, a solid white image with the same size as the incoming image is returned.

Extracting the alpha channel from [!DNL logo.png]:

```
>>> from s7vampy import *
>>> img = open_image("TestData/logo.png")
>>> img {name='TestData/logo.png', has_alpha=True, size=(256, 126)}
>>> img.extract_alpha() {name='TestData/logo.png', has_alpha=False, size=(256, 126)}
```

