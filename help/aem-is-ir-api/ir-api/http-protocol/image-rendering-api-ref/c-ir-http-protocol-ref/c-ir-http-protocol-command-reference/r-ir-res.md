---
description: Material resolution. Specifies the resolution of the repeatable texture or decal image.
solution: Experience Manager
title: res
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f207355d-5819-47fc-bda5-27a411449569
---
# res{#res}

Material resolution. Specifies the resolution of the repeatable texture or decal image.

 ` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Resolution; material resolution units (typically pixels per inch) (real). </p> </td> 
 </tr> 
</table>

In case of a decal material, `size=` prevails if both `size=` and `res=` are specified.

## Properties {#section-6a458ddc202f46e0b668c9f040a65cef}

Material attribute. Ignored by solid color materials. Only by cabinet and window coverings materials only if a texture is also used.

## Default {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, if the material is based on a catalog entry, otherwise `attribute::Resolution`, if `res= is` not specified or set to a value less than or equal to 0.

## See also {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Material Resolution](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b), [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988), [catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
