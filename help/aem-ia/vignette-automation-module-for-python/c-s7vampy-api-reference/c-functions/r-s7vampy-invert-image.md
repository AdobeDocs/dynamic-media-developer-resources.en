---
description: null
seo-description: null
seo-title: s7vampy.invert_alpha(image)
title: s7vampy.invert_alpha(image)
uuid: a267e822-103b-4393-a94d-ab0226e66634
index: y
internal: n
snippet: y
---

# s7vampy.invert_alpha(image){#s-vampy-invert-alpha-image}

<table id="table_EE3FE3CCAAF844F2AE840C0C4C7F3352"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Parameter: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> image</span> </p> <p>Path to image file. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Returns: </p> </td> 
   <td> <p><span class="codeph"><a href="../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a> </span> </p> <p> Inverted image. </p> </td> 
  </tr> 
 </tbody> 
</table>

Return an image where each color channel has been inverted.

This function is typically used with masks. Vignettes use mask images where white masks out the object from the background. If you encounter a mask image where blacks mask out the object from the background, you can use this function to invert that image so it can be used to build a vignette.

Inverting the mask stored in [!DNL mask.png]:

```
>>> from s7vampy import *
>>> img = open_image("TestData/mask.png")
>>> img {name='TestData/mask.png', has_alpha=False, size=(422, 640)}
>>> img2 = img.invert()
>>> img2 {name='TestData/mask.png', has_alpha=False, size=(422, 640)}
```

