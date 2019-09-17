---
description: Merge two images using the additive filter.
seo-description: Merge two images using the additive filter.
seo-title: s7vampy.merge_additive(image1, image2)
title: s7vampy.merge_additive(image1, image2)
uuid: 5846b55f-7b3a-4a44-a600-b740b647c1f7
---

# s7vampy.merge_additive(image1, image2){#s-vampy-merge-additive-image-image}

Merge two images using the additive filter.

<table id="table_EE3FE3CCAAF844F2AE840C0C4C7F3352"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Parameter image1: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> image1</span> </p> <p>Path to the base image file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameter image2: </p> </td> 
   <td colname="col2"> <p><span class="codeph"> image2</span> </p> <p>Path to the image file that you want to merge into the base image. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Returns: </p> </td> 
   <td> <p><span class="codeph"><a href="../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a> </span> </p> <p>Merged image. </p> </td> 
  </tr> 
 </tbody> 
</table>

Use this function to merge masks. Both images must be grayscale images and have the same dimensions.

Merging two masks:

```
    >>> from s7vampy import *
    >>> img = open_image("TestData/mask1.png")
    >>> img
    {name='TestData/mask1.png', has_alpha=False, size=(422, 640)}
    >>> img2 = open_image("TestData/mask2.png")
    >>> img2
    {name='TestData/mask2.png', has_alpha=False, size=(422, 640)}
    >>> merge_additive(img1, img2)
    {name='merge_additive', has_alpha=False, size=(422, 640)}
```

