---
title: template
description: Compositing template. Allows specifying a compositing template located in a catalog other than the main catalog.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
---
# template{#template}

Compositing template. Lets you specify a compositing template in a catalog other than the main catalog.

 `template= *`template`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>Template. </p></td> 
 </tr> 
</table>

*`template`* must be an image catalog entry with the template body contained in `catalog::Modifier`.

When `template=` is present, the object specified in the request path is not be applied as the source for layer 0. However, it can be referenced as a `src=` or `mask=` anywhere in the template by using the predefined path variable `$object$` as a `src=` value. `catalog::Modifier` of the object specified in the request path is only applied with the substitution of `$object$` within the template, while `catalog::PostModifier` is always applied.

Layer 0 is defined in the template body and can be an image, solid color, text, or nested or embedded request layer.

`catalog:PostModifier` of *`object`* is ignored when *`object`* is used with `template=`.

## Default {#section-9de53ea27c4b4fd4811e40e345d8ba05}

None.

## Properties {#section-daf3afb1d09c45a6a394468d0874c439}

Request attribute. Applies regardless of the current layer setting.

## Example {#section-9a4f260ed43342b186b0fe855f34bca6}

See the examples in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## See also {#section-067587444f774469931ecafd5a39834c}

[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Predefined Path Variable](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
