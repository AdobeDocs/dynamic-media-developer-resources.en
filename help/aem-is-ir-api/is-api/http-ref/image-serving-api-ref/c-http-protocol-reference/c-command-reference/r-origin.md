---
description: Layer origin.
seo-description: Layer origin.
seo-title: origin
solution: Experience Manager
title: origin
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# origin{#origin}

Layer origin.

 `origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>Pixel offset from the top-left corner of the layer rect (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normalized offset from the center of the layer rect (real, real). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>The layer rect always includes any modification by `extend=`.

Defines the alignment point of the layer rectangle, which is used to position the layer rectangle relative to layer 0 via `pos=`. `originN=0,0` positions the layer origin at the center of the layer rectangle. `originN=-0.5,-0.5` and `origin=0,0` is the top-left corner, and `originN=0.5,0.5` is the bottom-right corner of the layer rectangle.

## Properties {#section-60f639e36ada43d1abc6bfc100afc925}

Layer attribute. Applies to the current layer or to layer 0 if `layer=comp`. Not affected by layer transforms ( `crop=`, `scale=`, `rotate=`, `flip=`) applied to the layer source. Overrides `anchor=`. Ignored by effect layers.

## Default {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

If `origin=` is not specified, the layer origin is determined by applying the layer transforms to the image anchor. If the image anchor is not known, the center of the layer rectangle ( `originN=0,0`) is used.

## Example {#section-13e38d6e17be4e6cbc6b27fbde63b291}

See Example A in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## See also {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac) 
