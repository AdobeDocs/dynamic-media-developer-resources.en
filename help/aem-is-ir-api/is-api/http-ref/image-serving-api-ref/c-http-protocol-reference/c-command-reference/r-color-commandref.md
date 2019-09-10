---
description: Layer Color. Specifies the foreground color and opacity of solid color and effect layers, and the text box fill color for text layers.
seo-description: Layer Color. Specifies the foreground color and opacity of solid color and effect layers, and the text box fill color for text layers.
seo-title: color
solution: Experience Manager
title: color
topic: Scene7 Image Serving - Image Rendering API
uuid: 46b93609-02c0-47bf-97c0-e7b2e416d292
index: y
internal: n
snippet: y
---

# color{#color}

Layer Color. Specifies the foreground color and opacity of solid color and effect layers, and the text box fill color for text layers.

 ` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color </span> </span> </p> </td> 
  <td class="stentry"> <p>Gray, RGB, or CMYK color value, with or without alpha. </p> </td> 
 </tr> 
</table>

In case of image and text layers, `color=` fills transparent and semi-opaque areas within the bounding rectangle of the layer with the specified color* before* `rotate=` and `extend=` are applied.

## Properties {#section-d6e74c36a49547849212e4db8927e678}

Layer attribute. Applies to current layer or to layer 0 if `layer=comp`.

*`color`* is assumed to exist in the working color space corresponding to the pixel type of *`color`*. *`color`* is converted accurately if the layer image has a different pixel type at the time of merge.

## Default {#section-60611c72876b4c45b5c85ce35608e5ec}

No default for solid color and effect layers; a color must be specified. Defaults to 0,0,0,0 (fully transparent) for image and text layers.

## Example {#section-2d090493f4ec4e188bbc5565aa151a05}

In the following template fragment we set the text background to a 50% opaque color and use the same color to add a semi-transparent 10 pixel border around the layer 2 image:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## See also {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7) 
