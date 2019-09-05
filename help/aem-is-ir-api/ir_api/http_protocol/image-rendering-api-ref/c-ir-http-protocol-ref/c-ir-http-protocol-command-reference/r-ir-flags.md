---
description: Apply flags. Specifies additional render options.
seo-description: Apply flags. Specifies additional render options.
seo-title: flags
solution: Experience Manager
title: flags
topic: Scene7 Image Serving - Image Rendering API
uuid: 71fb3947-3577-4f77-a7d3-2b4a4eff4f85
index: y
internal: n
snippet: y
---

# flags{#flags}

Apply flags. Specifies additional render options.

 `flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Flag value. </p></td> 
 </tr> 
</table>

Currently used only for cabinet materials.

`flags=0` (default) renders upper cabinets with solid doors.

`flags=1` renders upper cabinets with glass doors (if the vignette was authored with glass doors).

## Properties {#section-a2b00d7bb15e449ea85178acb92d8285}

Material attribute. Ignored if not a cabinet material, or if the target cabinet object does not allow glass doors.

## Default {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` for no glass doors. 
