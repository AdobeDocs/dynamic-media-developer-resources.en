---
description: Normalized Coordinates. Used to specify relative positions within an image, such as image offsets or crop parameters, normalized to the size of the image.
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# coordN{#coordn}

Normalized Coordinates. Used to specify relative positions within an image, such as image offsets or crop parameters, normalized to the size of the image.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>coordinate offset normalized to the size of an image (real, real) </p></td> 
 </tr> 
</table>

Positive values move towards the bottom-right.

In many cases, the reference position is the center of the image. In this case, 0,0 corresponds to the center of the image, -0.5,-0.5 to the top-left corner, and 0.5,0.5 to the bottom-right corner.

Also used to specify image sizes or rectangle size relative to the size of layer 0. In this case, the values must be greater than 0. 0 may indicate that a specific default value should be used. 1,1 specifies a size equal to that of layer 0. 
