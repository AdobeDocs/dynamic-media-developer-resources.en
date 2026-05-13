---
title: op_usm
description: Unsharp-mask. Unsharp masks the layer or the final view image, after all scaling, if layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
TQID: 'https://experienceleague.adobe.com/Q2-9E1SNDgr8rGYWNKDLlVcQU85EhpEXhxAqF3WrJic'
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
# op_usm{#op-usm}

Unsharp-mask. Unsharp masks the layer or the final view image, after all scaling, if layer=comp.

The parameters are assumed to apply to the full resolution image and are scaled down when processing a downsampled image.

`op_usm= *`amount`*[, *`radius`*[, *`threshold`*[, *`monochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> amount</span></span> </p></td> 
  <td class="stentry"> <p>Filter strength factor (real 0…5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p></td> 
  <td class="stentry"> <p>Filter kernel radius in pixels (real 0…250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> threshold</span></span> </p></td> 
  <td class="stentry"> <p>Filter threshold level (int 0…255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monochrome</span></span> </p></td> 
  <td class="stentry"> <p>Set to 0 to apply to each color component separately or to 1 to apply only to the image brightness (intensity). </p> <p> <span class="codeph"><span class="varname"> monochrome</span></span> is ignored for grayscale images. </p></td> 
 </tr> 
</table>

The layer mask or composite mask is sharpened as well.

## Properties {#section-fb5311b34d164946b74dadb32359518a}

Layer attribute or view attribute. Applies to the current layer or to the final view image if `layer=comp`. Ignored by effect layers.

## Default {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` for no unsharp-masking effect.

## See also {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
