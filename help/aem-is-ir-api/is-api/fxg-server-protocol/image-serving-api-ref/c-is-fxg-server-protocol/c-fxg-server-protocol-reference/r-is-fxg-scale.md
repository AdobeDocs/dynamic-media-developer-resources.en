---
description: Scale image. Scales an image by factor relative to the full-resolution image.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
TQID: https://experienceleague.adobe.com/a-BnQdn22cOjQWjeayJzKc2gK3muEKYULXLFEhmnfgw
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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
