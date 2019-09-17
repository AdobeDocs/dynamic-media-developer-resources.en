---
description: Text layer attributes. Specifies additional attributes for text layers which are not available as rtf commands.
seo-description: Text layer attributes. Specifies additional attributes for text layers which are not available as rtf commands.
seo-title: textAttr
solution: Experience Manager
title: textAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 07b3d263-2ed6-4363-83e1-3b841e9967c5
---

# textAttr{#textattr}

Text layer attributes. Specifies additional attributes for text layers which are not available as rtf commands.

 ` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>Provides a means for scaling the text layer without changing font sizes. Higher resolution values increase the size of the rendered text relative to the canvas size; smaller values reduce the text size. Text resolution in dots per inch (int greater than 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing </span> </span> </p> </td> 
  <td class="stentry"> <p>Controls the anti-aliasing mode employed by the text rendering engine. </p> <p> <span class="codeph"> off | norm | crisp | sharp | strong | smooth </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> off </span> </p> </td> 
      <td class="stentry"> <p>Disable text anti-aliasing. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
      <td class="stentry"> <p>Enable standard text anti-aliasing mode (default). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> crisp </span> </p> </td> 
      <td class="stentry"> <p>Select Photoshop anti-aliasing mode <span class="codeph"> crisp </span> ( <span class="codeph"> textPs= </span> only). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> sharp </span> </p> </td> 
      <td class="stentry"> <p>Select Photoshop anti-aliasing mode <span class="codeph"> sharp </span> ( <span class="codeph"> textPs= </span> only). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> strong </span> </p> </td> 
      <td class="stentry"> <p>Select Photoshop anti-aliasing mode <span class="codeph"> strong </span> ( <span class="codeph"> textPs= </span> only). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Controls how res is used when rendering the text </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>Use the specified resolution. </p> <p>Use if the text is to be rendered in an exact size relative to the compositing canvas. Text may be clipped to the layer size (if specified) if the text box is too small. This is the only <span class="varname"> resMode </span> option supported by <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>Adjust the resolution automatically to best fill the layer rect with the text. </p> <p>Use to automatically adjust the text size so that the text box is filled as much as possible, without risk of truncation. If word wrap is enabled, text may be rewrapped at the final resolution. <span class="varname"> res </span> is ignored if <span class="codeph"> autoRes </span> is selected. Not supported by <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>Use the specified resolution; decrease it if necessary to prevent text being truncated to the layer rect. </p> <p>Use to render text at the exact specified resolution, as long as no clipping occurs. In case of clipping, the resolution is automatically decreased to ensure that all text is contained fully inside the text box. If word wrap is enabled, text may be rewrapped at the final resolution. Not supported by <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>If the text layer size is not specified with size= or if only the width is specified, 'autoRes' and 'maxRes' settings are ignored and the specified resolution is used to render the text. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>Specifies the wrapping mode. </p> <p> <span class="codeph"> wrap | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Disable word-wrap. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> wrap </span> </p> </td> 
      <td class="stentry"> <p>Enable standard word-wrap. </p> <p>Breaks long words if necessary. <span class="codeph"> textPs= </span> only supports <span class="codeph"> wrap </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Enable non-breaking word-wrap. </p> <p>Never breaks a word, even if it gets truncated at the end. Typically used in conjunction with <span class="codeph"> autoRes </span> or <span class="codeph"> maxRes </span> to ensure that long words are never broken. </p> </td> 
     </tr> 
    </table> </p> <p>Both <span class="codeph"> wrap </span> and <span class="codeph"> nbwrap </span> auto-wrap on word boundaries and hyphens. </p> </td> 
 </tr> 
</table>

## Properties {#section-114ca0b8585b403c873e2251478ad1d5}

Text layer attribute. Ignored by image, solid color, and effect layers. Applies to `layer=0` if specified for `layer=comp`.

## Default {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## See also {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) 
