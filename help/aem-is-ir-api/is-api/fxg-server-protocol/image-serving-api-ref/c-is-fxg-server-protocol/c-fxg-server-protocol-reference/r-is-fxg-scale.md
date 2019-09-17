---
description: Scale image. Scales an image by factor relative to the full-resolution image.
seo-description: Scale image. Scales an image by factor relative to the full-resolution image.
seo-title: scale
solution: Experience Manager
title: scale
topic: Scene7 Image Serving - Image Rendering API
uuid: db5bab94-e5c1-41fe-ab1b-5c62b6a798d0
---

# scale{#scale}

Scale image. Scales an image by factor relative to the full-resolution image.

 `scale= *`factor`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> factor</span></span> </p> </td> 
  <td class="stentry"> <p>Scale factor (real, &gt;0). </p></td> 
 </tr> 
</table>

## Default {#section-e9e53959b35844579f0f1d7721b71f8e}

If not specified, the image is used without scaling.

## Example {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5] 
