---
description: Flip Layer. Flips the layer horizontally, vertically, or both, after applying crop= and before rotate= and extend=.
seo-description: Flip Layer. Flips the layer horizontally, vertically, or both, after applying crop= and before rotate= and extend=.
seo-title: flip
solution: Experience Manager
title: flip
topic: Scene7 Image Serving - Image Rendering API
uuid: a9d36b86-92e9-4d49-bfbb-ff4fedf6c185
index: y
internal: n
snippet: y
---

# flip{#flip}

Flip Layer. Flips the layer horizontally, vertically, or both, after applying crop= and before rotate= and extend=.

 `flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Flip layer horizontally (left-right). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Flip layer vertically (up-down). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Flip both horizontally and vertically. </p> </td> 
 </tr> 
</table>

May also be applied to text layers.

Some commands, including `extend=`, implicitly apply to layer 0 instead of the composite layer when `layer=comp` is selected. In such scenarios, all commands that are assigned automatically to layer 0 will be applied before the commands which apply to `layer=comp`. Thus, when `layer=comp`, `extend=` is applied before `flip=`.

>[!NOTE]
>
>The flipped layer is positioned based on the layer anchor; different flip= values will result in different layer positions when the anchor is not located at the center of the layer.

## Properties {#section-294da2af7be746b5adfc35e29ee68217}

Layer command. Applies to the current layer or to the composite image if `layer=comp`. Ignored by effect layers.

## Default {#section-502044f81a89492198d5f12a738459ea}

None.

## See also {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) 
