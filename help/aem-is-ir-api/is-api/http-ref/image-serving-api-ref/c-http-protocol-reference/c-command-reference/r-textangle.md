---
description: Text render direction. Specifies the angle at which text specified with textPs= is laid out and rendered into the text box (defined with size= or textFlowPath=).
solution: Experience Manager
title: textAngle
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 102dbdc0-77b8-4c60-b456-6cf693e0b38b
---
# textAngle{#textangle}

Text render direction. Specifies the angle at which text specified with textPs= is laid out and rendered into the text box (defined with size= or textFlowPath=).

 ` textAngle= *`angle`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> angle </span> </p> </td> 
  <td class="stentry"> <p>Direction angle (degrees). </p> </td> 
 </tr> 
</table>

Positive values rotate the text clockwise; `textAngle=90` draws text top to bottom.

## Properties {#section-6d586a632daa4261a8ce62db56140b36}

Layer attribute. Applies to `layer=0` if `layer=comp`. Ignored if `textPs=` is not specified for this layer or if `textPath=` is specified.

## Default {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` for no rotation.

## See also {#section-dccc29ff33704061b2519b56b7be45fd}

[Text Formatting](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Text Positioning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
