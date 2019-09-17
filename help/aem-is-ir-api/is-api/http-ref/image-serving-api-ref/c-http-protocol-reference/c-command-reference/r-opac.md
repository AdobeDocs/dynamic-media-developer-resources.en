---
description: Adjust image opacity. Allows decreasing the foreground opacity of an image, text, solid color, or effect layer.
seo-description: Adjust image opacity. Allows decreasing the foreground opacity of an image, text, solid color, or effect layer.
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 268279bd-d777-4afe-b175-841af7e55406
---

# opac{#opac}

Adjust image opacity. Allows decreasing the foreground opacity of an image, text, solid color, or effect layer.

 `opac= *`opacity`*[, *`fillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> opacity</span> </p> </td> 
  <td class="stentry"> <p>Primary opacity (0…100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Fill opacity (0…100 int). </p></td> 
 </tr> 
</table>

The foreground opacity for an image layer is determined by the layer mask or the alpha channel of the image, or, if neither are present, it is 100%. The foreground opacity of a text layer is 100%, and that of a solid color layer is set by `color=`.

`opac=` never modifies the opacity of areas filled with `color=` or `bgColor=`, except the foreground areas of solid color and effect layers (set with `color=`).

When specified in an image, text, or solid color layer, *`opacity`* applies the entire layer, including all associated effect layers, while *`fillOpacity`* applies only to the primary layer contents. When specified in an effect layer, *`opacity`* applies to the effect layer, while *`fillOpacity`* is ignored.

The effective opacity for the main layer contents is ( *`opacity`* &#42; *`fillOpacity`* / 100). The effective opacity for effect layers is (main *`opacity`* &#42; effect *`opacity`* / 100).

## Properties {#section-ac3f136ff1584a2eab87500b7164f7fa}

Layer attribute. Applies to the current layer or to the composite image if `layer=comp`.

## Default {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, for no change in layer opacity.

## Example {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

The text opacity in this example is 90&#42;70/100=63%, and the effect layer opacity is 90&#42;50/100=45%.

## See also {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) 
