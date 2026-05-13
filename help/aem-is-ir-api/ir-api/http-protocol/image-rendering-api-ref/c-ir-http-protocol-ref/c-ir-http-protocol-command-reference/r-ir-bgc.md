---
title: bgc
description: Background color. Specifies the subtractive color for colorizable textures and decals.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
TQID: 'https://experienceleague.adobe.com/0Er9kHrfQj1lt14SlNJHxqddJZOp8BaO-lLYSqc5ajU'
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
# bgc {#bgc}

Background color. Specifies the subtractive color for colorizable textures and decals.

 `bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB or gray color value. </p></td> 
 </tr> 
</table>

Image Rendering's texture colorization algorithm is straightforward - the component values of `bgc=` are subtracted from the values of texture pixels; `color=` is added, and finally the result is clipped to `0,0,0` and `255,255,255`.

For typical uses of texture colorization, the value for `bgc=` might be the most important or dominant color in the texture image. Dynamic Media Image Authoring provides semi-automatic tools which extract reasonable `bgc=` color values from textures images.

When a texture material is applied to a non-texturable vignette object, `bgc=` is applied as the foreground color if `color=` is not specified.

## Properties {#section-b2db6f147d7f443ba9f671de04c2ef19}

Material attribute. Ignored by solid color and cabinet materials.

## Default {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` If the material is based on a catalog entry, otherwise `bgc=808080` (neutral gray).

## Example {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Colorize an apparel fabric whose texture has the dominant RGB color 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## See also {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
