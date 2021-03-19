---
description: Layer text (Adobe Photoshop compatible). Specifies the text body for a text layer.
seo-description: Layer text (Adobe Photoshop compatible). Specifies the text body for a text layer.
seo-title: textPs
solution: Experience Manager
title: textPs
uuid: 45e587b6-8dc8-408c-ade6-d70025fd1117
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# textPs{#textps}

Layer text (Adobe Photoshop compatible). Specifies the text body for a text layer.

 `textPs= *`string`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> string</span> </span> </p> </td> 
  <td class="stentry"> <p>Rich-text-formatted (RTF) string. </p></td> 
 </tr> 
</table>

All font, font color, and paragraph formatting control is achieved using RTF commands.

See [Text Formatting](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` supports extended features, such as justification, flowing of text into non-rectangular regions defined with `textFlowPath=` and/or `textFlowXPath=`, and rendering of text along arbitrary paths defined with `textPath=`.

## Properties {#section-a289dc26b6534b41998b1e241d5f2f92}

Layer attribute. Applies to `layer=0` if `layer=comp`. Mutually exclusive with `src=` and `text=` in the same layer. The last occurrence of `text=`, `textPs=`, and `src=` prevails and determines whether this is an image or a text layer. Ignored by effect layers.

## Default {#section-11c2ae2c96d64a0a9c207252df663e4d}

None.

## See also {#section-5c2b25767d2b47b5be817271ab12e13c}

[Text Formatting](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15) 
