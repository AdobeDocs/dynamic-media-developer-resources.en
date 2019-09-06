---
description: Select Layer. Selects a layer and starts a new layer definition segment in the command sequence.
seo-description: Select Layer. Selects a layer and starts a new layer definition segment in the command sequence.
seo-title: layer
solution: Experience Manager
title: layer
topic: Scene7 Image Serving - Image Rendering API
uuid: 64c2b136-7d99-4260-a6fa-623123e406d1
index: y
internal: n
snippet: y
---

# layer{#layer}

**Select Layer**. Selects a layer and starts a new layer definition segment in the command sequence.

`layer= *`n`*|comp[, *`name`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Number of layer to be selected (0 or greater int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>Select the composite image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>Layer name. </p></td> 
 </tr> 
</table>

All commands within the layer segment are applied to the specified layer. A layer segment is terminated by the next `layer=` or `effect=` command or the end of the request.

Specify `layer=comp` to select the composite image (or view, for some commands).

The layer number effectively specifies the z-order for the layer. Higher-numbered layers are placed on top of lower-numbered layers.

Layer numbers do not need to be consecutive. Layer 0 is required.

A name may be assigned to a layer with the `layer= *`n`*, *`name`*` command variant. Once a named layer is defined, it can be referenced with ` layer= *`name`*`, without needing to know the layer number. Multiple names may be assigned to the same layer, using multiple `layer= *`n`*, *`name`*` commands.

>[!NOTE]
>
>Layer 0 determines the overall size of the compositing canvas. All parts of layers falling outside the bounds of layer 0 are cropped off when the composite is built.

## Properties {#section-499963ee52c14f2898f0d0f90c1d01be}

Layer command. Substitution variable references are not supported in `layer=`.

`comp` is not permitted as a *`name`* string. An error is returned if the same *`name`* is assigned to more than one layer, or if a layer is referenced by *`name`* which has not been defined previously.

## Default {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Many commands and attributes apply to layer 0 if `layer=comp`.

## Special Cases {#section-e087cb2e3562473e8d391abfa3b9489f}

* If the same name is mapped to multiple layers (for example: `layer=1,image&layer=2,image`), an error occurs. 
* If the same name is mapped to a single layer multiple times (for example: `layer=1,image&layer=1,image`), scope is set as usual, without errors. 
* Multiple names for the same layer are supported.

  Either name can be used to reference the layer (for example: `layer=1,image&layer=1,picture`). 
* If a referenced name is never mapped to a layer number (for example: `layer=1,image&layer=picture`), an error occurs. 
* Substitution variables are not supported in layer modifiers (for example: `layer=$image$`).

  This applies to all permutations, not only to layer names but to layer modifiers in general. 

* All merging and overriding rules should work exactly as when same layer is referenced in multiple sources (request, pre or post modifier catalog records, macros, and so on).

## Example {#section-cc40de6a0a754178aa752601539c815b}

See the examples in [Templates](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e). 
