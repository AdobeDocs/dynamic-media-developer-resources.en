---
title: pos
description: Layer position.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
---
# pos{#pos}

Layer position.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixel offset from this layer's origin to the layer 0 origin (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normalized offset from this layer's origin to the layer 0 origin (real, real). </p></td> 
 </tr> 
</table>

If there is an image, text, and solid color layers, `pos=` specifies the position of a layer anchor relative to the layer 0 anchor. The `posN=` coordinate values are normalized relative to the actual layer 0 rect size.

If there are effect layers, `pos=` shifts the effect layer relative to the parent layer.

Positive values move the layer towards the right/bottom, and negative towards the left/top. In `posN=0.5,0.5`, it moves the layer by half the layer 0 width and height down and right.

## Properties {#section-51a60cdc52d040538fef378ace7c2e7d}

Layer attribute. Ignored if `layer=0` or `layer=comp`.

## Default {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. This coordinate places the layer anchor at the same location as the layer 0 anchor if this is an image, text, or solid color layer. Positions an effect layer directly over or under its parent layer.

## Example {#section-a89a02c22f6b4260bfcf7c842cd6069d}

See Example A in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## See also {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
