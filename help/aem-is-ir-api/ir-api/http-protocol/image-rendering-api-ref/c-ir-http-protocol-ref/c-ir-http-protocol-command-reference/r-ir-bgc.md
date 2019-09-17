---
description: Background color. Specifies the subtractive color for colorizable textures and decals.
seo-description: Background color. Specifies the subtractive color for colorizable textures and decals.
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 551a0da8-dd1f-484a-bf7e-f4896370340a
---

# bgc{#bgc}

Background color. Specifies the subtractive color for colorizable textures and decals.

 `bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB or gray color value. </p></td> 
 </tr> 
</table>

Image Rendering's texture colorization algorithm is quite simple - the component values of `bgc=` are subtracted from those of the texture pixels, `color=` is added, and finally the result is clipped to `0,0,0` and `255,255,255`.

For typical uses of texture colorization, the value for `bgc=` might be the most important or dominant color in the texture image. Scene7 Image Authoring provides semi-automatic tools which extract reasonable `bgc=` color values from textures images.

When a texture material is applied to a non-texturable vignette object, `bgc=` is applied as the foreground color if `color=` is not specified.

## Properties {#section-b2db6f147d7f443ba9f671de04c2ef19}

Material attribute. Ignored by solid color and cabinet materials.

## Default {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` if the material is based on a catalog entry, otherwise `bgc=808080` (neutral gray).

## Example {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Colorize an apparel fabric whose texture has the dominant RGB color 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## See also {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa) 
