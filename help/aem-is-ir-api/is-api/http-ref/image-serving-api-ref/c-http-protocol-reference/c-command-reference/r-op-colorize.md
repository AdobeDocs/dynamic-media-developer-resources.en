---
description: Colorize image. Colorizes the image data while preserving shadows and highlights.
solution: Experience Manager
title: op_colorize
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
---
# op_colorize{#op-colorize}

Colorize image. Colorizes the image data while preserving shadows and highlights.

 ` op_colorize= *`color`*[,off|norm[, *`contrast`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Replacement RGB color. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> off </span> </p> </td> 
  <td class="stentry"> <p>Disable automatic brightness compensation. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
  <td class="stentry"> <p>Enable automatic brightness compensation (default). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contrast </span> </p> </td> 
  <td class="stentry"> <p>Contrast range (real 0..100); set to 0 to preserve the input contrast. </p> </td> 
 </tr> 
</table>

The second argument specifies whether the brightness of the source image should be adjusted before colorizing. Specify `off` to disable the automatic brightness compensation or `norm` to adjust the brightness automatically so that the median value is at 50% intensity.

Set the *`contrast`* value to 0 to preserve the contrast range of the input image, or specify a desired contrast range with a value greater than 0. A value of 100 maximizes the contrast. Typical values might be between 30 and 70.

In addition to the built-in brightness and contrast adjustments, `op_brightness=` and `op_contrast=` may be used to further fine-tune the colorizing effect.

>[!NOTE]
>
>The colorizing algorithm uses only the luminance information in the image data. This conversion to grayscale is simple and not color-managed. `op_colorize` always outputs RGB data, even if the input is grayscale or CMYK.

## Properties {#section-c0f8bd424b864153a1108f384939f55b}

Layer command. Applies to the current layer or to the composite image if `layer=comp`. Ignored by effect layers.

*`color`* must be an RGB value; gray or CMYK *`color`* values are not supported.

The *`contrast`* value is ignored if brightness compensation is turned off.

*`color`* is assumed to exist in the working color space corresponding to the pixel type of *`color`*. *`color`* is converted accurately if the layer image has a different pixel type at the time of merge.

CMYK images are converted to RGB before the operation is applied.

## Default {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, for no colorization. The second and third arguments default to `norm,0`, for automatic brightness compensation and no contrast change.

## Example {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Adjust brightness and contrast dynamically before colorizing an image layer:

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

Use automatic brightness and contrast adjustment instead:

… `&op_colorize=a0b0c0,norm,50&`…

## See also {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
