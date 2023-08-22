---
title: text
description: Layer text. Specifies text and formatting content for a text layer.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
---
# text{#text}

Layer text. Specifies text and formatting content for a text layer.

 ` text= *`string`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> string </span> </p> </td> 
  <td class="stentry"> <p>Rich-text-formatted (RTF) string or plain-text string. </p> </td> 
 </tr> 
</table>

All font, font color, and paragraph formatting control is achieved using RTF commands. Refer to [Text Formatting](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) for additional information.

`text=` supports automatic scaling of the text to fill the layer rectangle specified with `size=`.

See [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` supports automatic sizing of the text layer to fit the rendered text (when `size=` is not specified or when only the width is specified). Note that in this case only one of the RTF alignment commands `\ql`, `\qr`, and `\qc` may be applied; an error is returned otherwise.

## Properties {#section-8c0f020094a44c6b858454ef91ab4edf}

Layer attribute. Applies to `layer=0` if `layer=comp`. Mutually exclusive with `src=` and `textPs=` in the same layer; the last occurrence of `text=`, `textPs=`, and `src=` prevails and determines whether this is an image or a text layer. Ignored by effect layers.

## Default {#section-58958671e0ad479e8d5f6c1d41d7dc74}

None.

## Example {#section-d011f765ec5c418d814a821019b0eef0}

See the examples in [Text Formatting](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) and [Example A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## See also {#section-207b779ab67342a5acd343e6bcc749c4}

[Text Formatting](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Text Positioning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
