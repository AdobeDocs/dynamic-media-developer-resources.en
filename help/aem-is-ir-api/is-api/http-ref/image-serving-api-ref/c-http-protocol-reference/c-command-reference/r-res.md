---
description: Resolution-based image scaling. Scales the image to the requested resolution.
solution: Experience Manager
title: res
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
---
# res{#res}

Resolution-based image scaling. Scales the image to the requested resolution.

 ` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Target resolution; typically in pixels per inch (real). </p> </td> 
 </tr> 
</table>

The scale factor is calculated by dividing *`val`* by `catalog::Resolution`. Note that this command does not affect the print resolution of the reply image.

To use this feature, the resolution of the original source images must be known and set in `catalog::Resolution`. Depending on the application, the resolution units may vary. For repeatable 2D textures or material swatches, such as wallpapers or fabrics, the resolution may be expressed as pixels/inch, or pixels/mm. Aerial photos and maps may be better served by pixels/mile or pixels/km. In any case, the units used for `catalog::Resolution` must be the same as the units used for `res=`.

In addition to obtaining images at precise resolutions, `res=` can also be used to combine multiple images at the same resolution, so that the items visible in these images are in accurate proportion to each other.

>[!NOTE]
>
>Normally, a composite image is resized to the target view size (specified by `wid=`, `hei=`, or `attribute::DefaultPix`) before it is returned to the client. To prevent this resizing and obtain an image with the exact resolution specified by `res=`, it may be necessary to disable view scaling by explicitly specifying `scl=1`. This instructs the server to crop the composite image to the target view size rather than scaling it.

## Properties {#section-fdbd16e59cff4952a3717146bc91412e}

Source image/mask attribute. Ignored by layers not associated with a source image or mask. Applied to layer 0 is specified for `layer=comp`. Ignored if either `scale=` or `size=` is specified for the same layer.

## Default {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

If not specified, `scale=` or `size=` determines the scale factor, or, if neither is specified, the image is used without scaling.

## Example {#section-eb06f333e08e4247971fb1b18922597b}

Retrieve a texture image at 12 pixels/inch object resolution for use with Image Rendering or Image Authoring. We specify loss-less PNG format and better quality resampling for best-possible quality,

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## See also {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
