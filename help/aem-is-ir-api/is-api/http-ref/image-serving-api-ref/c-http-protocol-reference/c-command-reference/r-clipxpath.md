---
description: Inverted Layer Clip Path. Specifies an exclusion clip path for the current layer. Any parts of the layer that are within the area defined by clipXPath= are rendered transparent.
seo-description: Inverted Layer Clip Path. Specifies an exclusion clip path for the current layer. Any parts of the layer that are within the area defined by clipXPath= are rendered transparent.
seo-title: clipXPath
solution: Experience Manager
title: clipXPath
uuid: a4062f3f-5dba-4514-acde-e1b7d608a2e9
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# clipXPath{#clipxpath}

Inverted Layer Clip Path. Specifies an exclusion clip path for the current layer. Any parts of the layer that are within the area defined by clipXPath= are rendered transparent.

 `clipXPath= *`pathDefinition`*`

`clipXPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>Name of path embedded in layer source image (ASCII only). </p></td> 
 </tr> 
</table>

See [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) for additional information, including a description of `*`pathName`*` and `*`pathDefinition`*`.

## Properties {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Layer attribute. Applies to the current layer or to the composite image if `layer=comp`. Ignored if `clipPath=` is not specified. Ignored by effect layers.

## Default {#section-d1986aa31af14767aeb1b4a57add67f4}

None.

## See also {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 
