---
description: Photoshop-style layer shadow and glow effects are implemented using special sub-layers (effect layers) which can be attached to any layer (the parent layer), including layer=0 and layer=comp.
seo-description: Photoshop-style layer shadow and glow effects are implemented using special sub-layers (effect layers) which can be attached to any layer (the parent layer), including layer=0 and layer=comp.
seo-title: Layer effects
solution: Experience Manager
title: Layer effects
topic: Scene7 Image Serving - Image Rendering API
uuid: 076e98de-cbbb-457b-984a-367a935b4356
index: y
internal: n
snippet: y
---

# Layer effects{#layer-effects}

Photoshop-style layer shadow and glow effects are implemented using special sub-layers (effect layers) which can be attached to any layer (the parent layer), including layer=0 and layer=comp.

While effect layers support a number of standard image and layer attributes and commands, they are not intended to be general purpose layers and do not support independent image or text data.

Any number of layer effects can be attached to a single parent layer.

## Inner and outer effects {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Inner effects* are rendered on top of the parent layer, and are visible only in opaque areas of the parent layer. *Outer effects* are rendered behind the parent layer (thus they will never be visible within opaque areas of the parent layer) and can be positioned anywhere within the compositing canvas. An inner or outer effect is chosen by assigning a positive or negative effect layer number with the `effect=` command. The `effect=` command also controls the z-ordering amongst multiple effect layers attached to the same parent layer.

## Relationship to parent layer {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Effect layers are automatically sized and positioned to coincide with the parent layer (i.e. the effect layer inherits the `size=` and `origin=` values of the parent layer). `pos=` can be used to shift the effect layer away from the parent layer, as is typically required for drop and inner shadow effects. While for standard layers `pos=` specifies an offset between the origins of this layer and layer 0, for effect layers `pos=` specifies the offset between the origins of the effect layer and the parent layer.

## Supported commands and attributes {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

Effect layers accept the following commands and attributes:

* `blendMode=` 
* `effect=` 
* `color=` 
* `maskUse=` 
* `opac=` 
* `op_grow=` 
* `op_blur=` 
* `op_noise=` 
* `pos=`

All other image and layer commands contained in effect layers are ignored.

## Default effect macros {#section-a01e8dcc87c94495b54a6dfb21d2a718}

To facilitate layer effects use, IS provides two macros with the default image catalog, `$shadow$` and `$glow$`, which provide default values for effect layer attributes which are similar to Photoshop layer effects. The following table lists which effect command and macro should be used to implement the default layer effects. Naturally, any of the attributes specified in the macros can be modified in the URL, or alternative macros can be created to implement custom layer effects. 

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Desired effect</b> </th> 
   <th class="entry"> <b> Command</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Drop Shadow </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Inner Shadow </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Outer Glow </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Inner Glow </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Examples {#section-4c449fdf707b43858917fb271fa1fe96}

Add a three pixel wide, red border with 50% opacity to a layer:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

The border will follow the contours of the image's alpha channel or mask. Setting `effect=1` would place the border on the inside edge instead.

Add a bluish drop shadow to an image, using the default effect settings (except for the color):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` adds a little margin to the bottom right edges of the image, which prevents the drop shadow from being clipped to the image bounds.

## See also {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [Command Macros%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9) 
