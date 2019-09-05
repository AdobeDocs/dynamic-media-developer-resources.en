---
description: Advanced render settings. Specifies an advanced render settings, to be applied when rendering the current selection.
seo-description: Advanced render settings. Specifies an advanced render settings, to be applied when rendering the current selection.
seo-title: rs
solution: Experience Manager
title: rs
topic: Scene7 Image Serving - Image Rendering API
uuid: c584e41f-8155-4076-a0ab-d7084200a928
index: y
internal: n
snippet: y
---

# rs{#rs}

Advanced render settings. Specifies an advanced render settings, to be applied when rendering the current selection.

 `rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Render settings string. </p></td> 
 </tr> 
</table>

Used for fine-tuning render appearance. Use the render feature of the Vignette Authoring Tool (part of the Scene7 Image Authoring package) to create render settings strings.

## Properties {#section-9a2b2228789046658cb80eddf343af75}

Material attribute.

## Default {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Example {#section-47e4811882574441a4d517e42a35f352}

After some experimentation in Image Authoring, it is determined that unsharp-masking (USM) provides the correct amount of sharpening for the given application and material. The render settings string that configures USM is copied to the `rs=` command to use with this material:

`…&rs=U2V20W50X2&…`

## See also {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711) 
