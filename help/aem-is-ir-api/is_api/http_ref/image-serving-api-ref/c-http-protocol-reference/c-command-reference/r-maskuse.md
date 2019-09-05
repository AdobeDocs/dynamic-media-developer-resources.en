---
description: Image mask usage. Specifies how the mask or alpha channel of the image is used for operations on the image (for example, colorize=). When specified in an effect layer, it allows applying the effect to the background area of parent layer or to the entire parent layer rectangle.
seo-description: Image mask usage. Specifies how the mask or alpha channel of the image is used for operations on the image (for example, colorize=). When specified in an effect layer, it allows applying the effect to the background area of parent layer or to the entire parent layer rectangle.
seo-title: maskUse
solution: Experience Manager
title: maskUse
topic: Scene7 Image Serving - Image Rendering API
uuid: 71f0d878-0ba8-4ffb-a706-42ea81e6bd51
index: y
internal: n
snippet: y
---

# maskUse{#maskuse}

Image mask usage. Specifies how the mask or alpha channel of the image is used for operations on the image (for example, colorize=). When specified in an effect layer, it allows applying the effect to the background area of parent layer or to the entire parent layer rectangle.

 `maskUse=norm|invert|off`

The following table illustrates the effect of `maskUse=` depending on availability and type of the mask (alpha channel) associated with the layer image.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Value</b> </th> 
   <th class="entry"> <b> No mask</b> </th> 
   <th class="entry"> <b> Unassociated alpha (or separate mask image)</b> </th> 
   <th class="entry"> <b> Associated (pre-multiplied) alpha</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> off </span> </p> </td> 
   <td> <p> Opaque image rectangle </p> </td> 
   <td> <p> Opaque image rectangle </p> </td> 
   <td> <p> Foreground area of image over rectangle filled with solid black </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norm </span> </p> </td> 
   <td> <p> Opaque image rectangle </p> </td> 
   <td> <p> Foreground area of image </p> </td> 
   <td> <p> Foreground area of image or layer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invert </span> </p> </td> 
   <td> <p> Hidden layer </p> </td> 
   <td> <p> Background area of image </p> </td> 
   <td> <p> Background area of image or layer filled with solid black </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f36ad1af348e45aeb3eb336544df30b0}

Image or layer attribute. Applies to layer 0 if `layer=comp`. If specified in an effect layer, the command modifies the mask inherited from the parent layer.

The behavior of `maskUse=` is undefined and unsupported when specified with text or solid color layers when no image mask is applicable (specified with `mask=` or `catalog::Mask`).

## Default {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Example {#section-daa371e9be5547368ff6772342acba0a}

Colorize the background area of an image; the image foreground is defined by a separate mask image. This is achieved by layering the colorized image background on top if the unmodified image:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## See also {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](r_is_http_color.md#reference_0FDB264A3AED4BD78451BB55311F6E93) , [mask=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)  
