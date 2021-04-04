---
description: Normalized Size. Used to specify image sizes or rectangle sizes, normalized relative to the size of layer 0 or some other image.
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
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
