---
description: Text flow area. Specifies one or more regions into which text specified with textPs= should be flowed.
seo-description: Text flow area. Specifies one or more regions into which text specified with textPs= should be flowed.
seo-title: textFlowPath
solution: Experience Manager
title: textFlowPath
topic: Scene7 Image Serving - Image Rendering API
uuid: 5449d78f-e56b-4afb-a05a-7cf8f1f37278
index: y
internal: n
snippet: y
---

# textFlowPath{#textflowpath}

Text flow area. Specifies one or more regions into which text specified with textPs= should be flowed.

 ` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p> </td> 
 </tr> 
</table>

See [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) for additional information, including a description of *`pathDefinition`*.

The RTF margin commands `\margl`, `\margr`, `\margt`, and `\margb` are ignored when `textFlowPath=` is present. If no path definition is specified, `textFlowPath=` is ignored.

## Properties {#section-b68dc887c6534ce8982cad740b3aeaa4}

Text layer attribute ( `textPs=` only). Ignored by other layers. Applies to `layer=0` if specified for `layer=comp`.

## Default {#section-68c4559b9e8242059b82e5a39a455dfc}

Same as the layer rectangle; text fills the entire layer rectangle.

## See also {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), [Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f) 
