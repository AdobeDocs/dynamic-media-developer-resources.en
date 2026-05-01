---
title: op_growMaskR
description: Dilate/erode image. Applies a morphological dilate (radius > 0) or erode (radius < 0) to the mask data.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
TQID: https://experienceleague.adobe.com/ASrY3tIko05yVSSPdwbfrR79gpKhzVqk0blIQkiJbe0
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
# op_growMaskR{#op-growmaskr}

Dilate/erode image. Applies a morphological dilate (radius > 0) or erode (radius < 0) to the mask data.

 `op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode radius in pixels where <span class="codeph"><span class="varname"> radiusR</span></span> is applied as is, regardless of whether the mask is downsampled (int -100..100). </p></td> 
 </tr> 
</table>

Primarily used to slightly grow or shrink a mask to avoid artifacts around the edge of the mask.

## Properties {#section-b1c66d65168d4ea695e8662ea690bd4e}

Applies to the current layer or to layer `0` if `layer=comp`.

## Default {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, for no change.

## See also {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Layer Effects](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
