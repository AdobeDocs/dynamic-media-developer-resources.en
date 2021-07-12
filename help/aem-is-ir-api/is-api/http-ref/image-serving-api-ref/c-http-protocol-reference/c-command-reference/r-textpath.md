---
description: Text path. Specifies the path to be used as the baseline for the text provided with textPs=.
solution: Experience Manager
title: textPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
---
# textPath{#textpath}

Text path. Specifies the path to be used as the baseline for the text provided with textPs=.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

See [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) for additional information, including a description of *`pathDefinition`*.

>[!NOTE]
>
>Different from `clipPath=`, text paths are not closed automatically when 'z' or 'Z' is not specified at the end of a sub-path.

*`pathDefinition`* may include multiple sub-paths. Text is rendered on the sub-paths in the order specified.

The RTF commands `\ql`, `\qc`, `\qr`, `\li`, and `\ri` can be used to position the rendered text along the path.

## Properties {#section-068137df436c46b9b55d271eb60e7285}

Text layer attribute ( `textPs=` only). Ignored by other layers. Applies to `layer=0` if specified for `layer=comp`. Ignored if `textPs=` are present.

An error is returned if a layer includes both `textPath=` and `textFlowPath=`.

## Default {#section-697b1f2cfc43498080a31327e6eb173d}

None, for standard text rendering.

## See also {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
