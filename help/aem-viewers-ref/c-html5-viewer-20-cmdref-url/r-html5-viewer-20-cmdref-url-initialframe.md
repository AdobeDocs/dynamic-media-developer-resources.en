---
title: initialFrame
description: Parameter common to all viewers.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
TQID: https://experienceleague.adobe.com/NiBLo-70aElnEld3rIL3dVigM2UoxKNVVKk3ZX1Jjcg
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# initialFrame{#initialframe}

Parameter common to all viewers.

>[!NOTE]
>
>This command does not apply to Video Image Viewer.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies a zero-based frame index that the viewer displays on load. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>A zero-based index of the page within the spread when the device is in portrait orientation. For a "left-to-right" environment, <span class="codeph"> 0</span> means "left page" and <span class="codeph"> 1</span> means "right page". For a "right-to-left" environment, it is opposite: <span class="codeph"> 0</span> means "right page" and <span class="codeph"> 1</span> means "left page". </p> <p>If not specified, <span class="codeph"> 0</span> is assumed by default. Ignored when device is in landscape orientation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Default {#section-d411e450028c460392cb8508f8ccc5d9}

No default.

## Example {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
