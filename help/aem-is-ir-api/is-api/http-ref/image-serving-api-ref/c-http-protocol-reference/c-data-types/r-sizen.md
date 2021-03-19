---
description: Normalized Size. Used to specify image sizes or rectangle sizes, normalized relative to the size of layer 0 or some other image.
seo-description: Normalized Size. Used to specify image sizes or rectangle sizes, normalized relative to the size of layer 0 or some other image.
seo-title: sizeN
solution: Experience Manager
title: sizeN
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# sizeN{#sizen}

Normalized Size. Used to specify image sizes or rectangle sizes, normalized relative to the size of layer 0 or some other image.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>normalized width and height relative to another image (real, real, greater than 0) </p></td> 
 </tr> 
</table>

Both *nx* and *ny* must be greater than 0. 0,0 may indicate that a specific default size should be used. 1,1 specifies a size equal to the reference image. 
