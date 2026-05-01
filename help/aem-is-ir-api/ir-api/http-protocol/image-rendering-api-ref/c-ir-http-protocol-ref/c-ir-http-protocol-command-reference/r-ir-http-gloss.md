---
title: gloss
description: Material surface glossiness. Specifies the relative glossiness of the material surface. Used to select the illumination map and control rendering of gloss effects and 3D reflections.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
TQID: https://experienceleague.adobe.com/id0qagj6eHzdY8ptPKE0bSNtF5xFLp0uajc45jmMM7k
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
# gloss{#gloss}

Material surface glossiness. Specifies the relative glossiness of the material surface. Used to select the illumination map and control rendering of gloss effects and 3D reflections.

 `gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Gloss (0…100 percent) or -1 for the default (reference) gloss value. </p></td> 
 </tr> 
</table>

Higher gloss values typically cause stronger, sharper reflections, and, if gloss effects are enabled in the vignette, strengthens specular highlights on the material surface, mostly by increasing the illumination contrast. Each material type ( `type=`) defines a minimum and a maximum render effect. For some material types (for example, wall paper), `gloss=` has minimal any impact on the appearance of the render effect, while for other material types (for example, stone or ceramic), the effect is substantially more pronounced.

If `illum=-1` and if the vignette defines multiple illumination maps, `gloss=` selects the illumination map used for the current render operation. The renderer chooses the illumination map whose gloss value is closest to the specified gloss.

`gloss=-1` Selects the reference gloss value of the selected illumination map, as defined in the view properties of the vignette. This value ensures that the illumination map is used exactly as authored, without further modification, even if gloss effects are enabled. If `illum=-1` then the reference gloss value of the first illumination map in the vignette view is used.

## Properties {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Material attribute. Ignored if the vignette does not define multiple illumination maps. Or, if `illum=` is specified, if the vignette does not include 3D reflection data. Or, if the current object does not support 3D reflections, or if gloss effects are disabled in the vignette.

## Default {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` If the material is based on a catalog entry, otherwise the reference gloss value of the default illumination map or the illumination map specified by `illum=`.

## See also {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
