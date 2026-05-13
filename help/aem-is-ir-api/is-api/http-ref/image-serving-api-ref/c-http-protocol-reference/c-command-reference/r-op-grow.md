---
title: op_grow
description: Dilate/erode image. Applies a morphological dilate (radius > 0) or erode (radius < 0) to the image data.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
TQID: 'https://experienceleague.adobe.com/vNFqqzcSqktgB5ohUZjqf0RtQNOD-t7fxITR2gZl-T4'
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
# op_grow{#op-grow}

Dilate/erode image. Applies a morphological dilate (radius > 0) or erode (radius < 0) to the image data.

 `op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode radius in pixels (int -100..100). </p></td> 
 </tr> 
</table>

`*`radius`*` is in pixels relative to the composite image. If the image is color, each component is processed independently.

Primarily used to modify the size of layer effects. Also useful to achieve special effects on text layers or solid color layers with masks.

## Properties {#section-b1c66d65168d4ea695e8662ea690bd4e}

Layer attribute. Applies to the current layer or to the composite image if `layer=comp`.

## Default {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, for no change.

## See also {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Layer Effects](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
