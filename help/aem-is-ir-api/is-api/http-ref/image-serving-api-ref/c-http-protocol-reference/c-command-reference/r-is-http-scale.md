---
title: scale
description: Scale image. Scales a layer source image by factor relative to the full-resolution image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
TQID: 'https://experienceleague.adobe.com/qC-yBofpV9CNTTjb8Ll1EYV6Q1YA0BUsLLEHadfLAu8'
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

Scale image. Scales a layer source image by factor relative to the full-resolution image.

 `scale= *`factor`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> factor</span> </p> </td> 
  <td class="stentry"> <p>Scale factor (real, greater than 0.0). </p></td> 
 </tr> 
</table>

No scaling is applied when `scale=1`. *`factor`* smaller than 1.0 down-scales and larger than 1.0 enlarges the source image.

## Properties {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Source image/mask attribute. Ignored if `size=` is specified as well for the current layer. Overrides `res=`. Applies to layer 0 if specified for `layer=comp`. Ignored if the layer is not associated with an image or mask.

## Default {#section-26e64904362342a5a62c5f6598f330c4}

If not specified, `res=` is used. If `res=` is not specified, the image is used without scaling.

## See also {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
