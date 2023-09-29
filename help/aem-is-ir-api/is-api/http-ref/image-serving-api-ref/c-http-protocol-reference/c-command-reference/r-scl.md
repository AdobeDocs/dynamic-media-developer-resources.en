---
title: scl
description: Scale view. Scales the composite image by the inverse of invFactor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
---
# scl{#scl}

Scale view. Scales the composite image by the inverse of invFactor.

 `scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>Inverse scale factor (real greater than 0.0). </p></td> 
 </tr> 
</table>

No scaling is applied when `scl=1`. An *`invFactor`* value that is larger than 1.0 down-scales and smaller than 1.0 enlarges the composite image.

If `scl=` is specified, and `wid=` and/or `hei=` are present as well, the image is cropped to `wid=` and/or `hei=` after scaling.

>[!NOTE]
>
>An error is returned if the calculated or default reply image size is larger than `attribute::MaxPix`.

## Properties {#section-60af012719db477db4a4703e9a6da5f5}

View Attribute. It applies regardless of the current layer setting.

## Default {#section-32502fa218a24e1f9c65f41c0260b56a}

If neither `wid=`, `hei=`, nor `scl=` are specified, the reply image either has the size of the composite image or `attribute::DefaultPix`, whichever is smaller.

## Example {#section-a33f6239476a4b438d939656ad99aa76}

See the example in [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) for a common application of `scl=`.

## See also {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
