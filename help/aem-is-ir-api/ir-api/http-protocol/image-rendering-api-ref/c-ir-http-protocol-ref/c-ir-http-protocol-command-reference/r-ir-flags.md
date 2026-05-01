---
title: flags
description: Apply flags. Specifies additional render options.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
TQID: https://experienceleague.adobe.com/iAa5eazr9MdJox0-9FurnNlutMnxy2-9KKzCVNcA-k8
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
# flags {#flags}

Apply flags. Specifies additional render options.

 `flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Flag value. </p></td> 
 </tr> 
</table>

Currently used only for cabinet materials.

`flags=0` (default) Renders upper cabinets with solid doors.

`flags=1` Renders upper cabinets with glass doors (if the vignette was authored with glass doors).

## Properties {#section-a2b00d7bb15e449ea85178acb92d8285}

Material attribute. Ignored if not a cabinet material, or if the target cabinet object does not allow glass doors.

## Default {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` For no glass doors.
