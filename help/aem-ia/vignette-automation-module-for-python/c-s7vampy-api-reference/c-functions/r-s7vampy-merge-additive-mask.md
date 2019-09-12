---
description: Merge image2 in to a masked region of image1 using the additive filter.
seo-description: Merge image2 in to a masked region of image1 using the additive filter.
seo-title: s7vampy.merge_additive_mask(image1, image2, mask)
title: s7vampy.merge_additive_mask(image1, image2, mask)
uuid: 727bc9c7-5142-4d06-9343-8cf23db49191
index: y
internal: n
snippet: y
---

# s7vampy.merge_additive_mask(image1, image2, mask){#s-vampy-merge-additive-mask-image-image-mask}

Merge image2 in to a masked region of image1 using the additive filter.

<table id="table_EE3FE3CCAAF844F2AE840C0C4C7F3352"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Parameter image1: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> image1</span> </p> <p>Path to the base image file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameter image2: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> image2</span> </p> <p>Path to the image file that you want to merge into <span class="codeph"> image1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameter mask: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> mask</span> </p> <p>Masked region in <span class="codeph"> image1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Returns: </p> </td> 
   <td> <p><span class="codeph"><a href="../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a> </span> </p> <p>Merged image. </p> </td> 
  </tr> 
 </tbody> 
</table>

This function is used to merge illumination maps. The images and the mask are all required to be grayscale images and have the same dimension.

Merge two illumination maps:

```
    >>> from s7vampy import *
    >>> img = open_image("TestData/illum1.png")
    >>> img
    {name='TestData/illum1.png', has_alpha=False, size=(422, 640)}
    >>> img2 = open_image("TestData/illum2.png")
    >>> img2
    {name='TestData/illum2.png', has_alpha=False, size=(422, 640)}
    >>> mask = open_image("TestData/mask1.png")
    >>> mask
    {name='TestData/mask1.png', has_alpha=False, size=(422, 640)}
    >>> merge_additive_mask(img1, img2, mask)
    {name='merge_additive_mask', has_alpha=False, size=(422, 640)}
```

